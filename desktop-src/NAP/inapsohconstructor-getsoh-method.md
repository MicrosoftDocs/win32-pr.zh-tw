---
title: 'INapSoHConstructor GetSoH 方法 (NapProtocol .h) '
description: 抓取已建立的 SoHRequest 或 SoHResponse 封包。
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- GetSoH 方法 NAP
- GetSoH 方法 NAP，INapSoHConstructor 介面
- INapSoHConstructor 介面 NAP，GetSoH 方法
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094487"
---
# <a name="inapsohconstructorgetsoh-method"></a>INapSoHConstructor：： GetSoH 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSoHConstructor：： GetSoH** 方法會抓取已建立的 SoHRequest 或 SoHResponse 封包。

## <a name="syntax"></a>語法


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*soh* \[擴展\]
</dt> <dd>

指向已建立之 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 或 **SoHResponse** 封包指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                   |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>NapProtocol。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





