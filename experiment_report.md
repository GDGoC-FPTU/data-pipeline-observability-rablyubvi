# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-2A202600428
**Name:** Trần Ngô Hồng Hà
**Date:** 15/04/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) |Based on my data, the best choice is Laptop at $1200| | |
| Garbage Data (`garbage_data.csv`) |Based on my data, the best choice is Nuclear Reactor at $999999 | | |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

(Viet nhan xet cua ban o day — it nhat 50 tu)

(Hay phan tich cac van de nhu Duplicate IDs, wrong data types, outliers, null values
va giai thich tai sao chung anh huong den ket qua cua Agent.)
Với garbage data, RAG-like stimulate agent với querry "what is the best electronics products", agent sẽ check dựa trên giá và category. Nuclear Reactor được gán cho category là electronics, và có giá là 99999, mặc nhiên cao nhất. Vấn đề ở đây là dòng dữ liệu này vừa là outliers, vừa là dữ liệu bị gán sai thuộc tính
---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

(Viet ket luan cua ban o day)
Prompt có chi tiết, có tốt đến đâu, nhưng agent cũng chỉ dựa trên data có sẵn để gen ra câu trả lời. Vậy nên nếu chất lượng data tệ thì chất lượng đầu ra cũng không thể tốt được 
