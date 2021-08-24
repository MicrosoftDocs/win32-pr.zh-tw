---
description: 設定目的電腦系統上的封包 Exchange (IPX) 虛擬網路編號。
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetIPXVirtualNetworkNumber 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: 37af763450eab2fdba373fe21bfde5c0b4e1e38fda1f42aff59c425ba6b10000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079772"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a>Win32 >networkadapterconfiguration 類別的 SetIPXVirtualNetworkNumber 方法 \_

設定目的電腦系統上的封包 Exchange (IPX) 虛擬網路編號。 Windows 2000 和 Windows NT 3.51 或更新版本都會使用內部網路編號進行內部路由。 內部網路編號也稱為虛擬網路編號。 它可唯一識別網路上的電腦系統。 方法會傳回一個整數值，這個值的意義如下：

## <a name="syntax"></a>語法


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IPXVirtualNetNumber* \[在\]
</dt> <dd>

此系統的虛擬網路編號。

</dd> </dl>

## <a name="return-value"></a>傳回值

<dl> <dt>

**成功完成，不需要重新開機** (0) 
</dt> <dt>

**成功完成，需要重新開機** (1) 
</dt> <dt>

**此平臺 (64) 不支援的方法**
</dt> <dt>

**未知的失敗** (65) 
</dt> <dt>

**不正確子網路遮罩** (66) 
</dt> <dt>

**處理傳回的實例時發生錯誤** (67) 
</dt> <dt>

**不正確輸入參數** (68) 
</dt> <dt>

 (69) **指定超過5個閘道**
</dt> <dt>

**不正確 IP 位址** (70) 
</dt> <dt>

**不正確閘道 IP 位址** (71) 
</dt> <dt>

**存取所要求資訊** 的登錄時發生錯誤 (72) 
</dt> <dt>

**不正確功能變數名稱** (73) 
</dt> <dt>

**不正確主機名稱** (74) 
</dt> <dt>

**未定義任何主要/次要 WINS 伺服器** (75) 
</dt> <dt>

**不正確檔** (76) 
</dt> <dt>

**不正確系統路徑** (77) 
</dt> <dt>

檔案 **複製失敗** (78) 
</dt> <dt>

 (79) 的 **安全性參數無效**
</dt> <dt>

**無法設定 tcp/ip 服務** (80) 
</dt> <dt>

**無法設定 DHCP 服務** (81) 
</dt> <dt>

**無法更新 DHCP 租用** (82) 
</dt> <dt>

**無法釋放 DHCP 租用** (83) 
</dt> <dt>

**介面卡上未啟用 IP** (84) 
</dt> <dt>

**未在介面卡上啟用 IPX** (85) 
</dt> <dt>

**畫面格/網路編號界限錯誤** (86) 
</dt> <dt>

**不正確框架類型** (87) 
</dt> <dt>

 (88) 的 **網路編號無效**
</dt> <dt>

 (89) **重複的網路編號**
</dt> <dt>

**參數超出範圍** (90) 
</dt> <dt>

**拒絕存取** (91) 
</dt> <dt>

**記憶體不足** (92) 
</dt> <dt>

**已存在** (93) 
</dt> <dt>

**找不到路徑、檔案或物件** (94) 
</dt> <dt>

**無法通知服務** (95) 
</dt> <dt>

**無法通知 DNS 服務** (96) 
</dt> <dt>

**介面無法** 設定 (97) 
</dt> <dt>

**並非所有 DHCP 租用都** 可以釋出/更新 (98) 
</dt> <dt>

**未在介面卡上啟用 DHCP** (100) 
</dt> <dt>

**其他** (101 – 4294967295) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




