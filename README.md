# nodemawari
Hướng dẫn chạy node MAWARI
❇️ Các bước chạy node:
Yêu cầu máy phải có Docker ( Win or Ubuntu ) Hướng dẫn trên Ubuntu

1: https://testnet.mawari.net/mint

- Kết nối ví
- Faucet
- Mint NFT ( 1 ví max 3 NFT )
 
<img width="1182" height="894" alt="image" src="https://github.com/user-attachments/assets/04211dab-99e3-41ef-a470-2b53bcc3f80f" />

2: Khởi tạo node và chạy node, chạy lần lượt các lệnh theo thứ tự từ trên xuống dưới

```bash
export MNTESTNET_IMAGE=us-east4-docker.pkg.dev/mawarinetwork-dev/mwr-net-d-car-uses4-public-docker-registry-e62e/mawari-node:latest
```

```bash
export OWNER_ADDRESS=0xĐịaChỉVíCủaBạn
```


* Lệnh kiểm tra xem đã đúng địa chỉ ví chưa: 

```bash
echo $OWNER_ADDRESS
```


<img width="1051" height="82" alt="image" src="https://github.com/user-attachments/assets/67688c5d-2dec-4558-ad4f-d86582775a13" />

* Lệnh khởi chạy node: 

```bash
mkdir -p ~/mawari && docker run --pull always -v ~/mawari:/app/cache -e OWNERS_ALLOWLIST=$OWNER_ADDRESS $MNTESTNET_IMAGE
```

* Khi chạy node xong để ý code sẽ hiện ra dòng:
[INFO]  Using burner wallet {"address": "0x123456"} 

Cái address burner lưu lại, mỗi người sẽ ra 1 địa chỉ khác nha.
- Mở ví đã có token faucet và gửi 1 Token MAWARI vào địa chỉ ví đó
<img width="423" height="22" alt="image" src="https://github.com/user-attachments/assets/096ac89a-6707-4a32-8262-f5e8747dd25e" />


3: Delegate node : https://app.testnet.mawari.net/licenses
- Kết nối ví
- Chọn Delegate
- Dán địa chỉ ví Bunder vào 

3 License ID có thể chạy chung 1 địa chỉ Burner 

4: Điền form feedback: https://docs.google.com/forms/d/e/1FAIpQLScn-qN1oNbd_At0UEIK5bJFPlEEouGh49f_MWHS7nhGeNDe8A/viewform

