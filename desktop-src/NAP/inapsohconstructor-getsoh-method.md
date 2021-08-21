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
ms.openlocfilehash: d3d411d57ae77a1e5bf8c04ca0d9d980a9c33e9fcf15eb05f157ddeda98711c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133821"
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



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                   |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>NapProtocol。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





