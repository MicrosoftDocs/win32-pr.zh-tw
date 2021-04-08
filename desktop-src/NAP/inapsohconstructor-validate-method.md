---
title: 'INapSoHConstructor Validate 方法 (NapProtocol .h) '
description: 檢查 SoH 封包的有效性。
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- 驗證方法 NAP
- 驗證方法 NAP、INapSoHConstructor 介面
- INapSoHConstructor 介面 NAP，Validate 方法
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686184"
---
# <a name="inapsohconstructorvalidate-method"></a>INapSoHConstructor：： Validate 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSoHConstructor：： Validate** 方法會檢查 SoH 封包的有效性。

## <a name="syntax"></a>語法


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*soh* \[在\]
</dt> <dd>

結構化 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包的指標。

</dd> <dt>

*isRequest* \[在\]
</dt> <dd>

如果封包是 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則 **布林****值為 TRUE** ，如果是 **SoHResponse**，則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                  | SoH 封包有效。<br/>                                |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>        | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>         | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**NAP \_ E \_ 不正確封 \_ 包**</dt> </dl> | SoH 封包無效。<br/>                              |



 

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

 

 





