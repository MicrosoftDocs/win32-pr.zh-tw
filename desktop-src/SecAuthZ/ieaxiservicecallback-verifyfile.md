---
description: 針對指定的 ActiveX 物件執行安全性檢查，並傳回下載對應 .cab 檔案的位置。
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: IeAxiServiceCallback：： VerifyFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513913"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>IeAxiServiceCallback：： VerifyFile 方法

**VerifyFile** 方法會在指定的 ActiveX 物件上執行安全性檢查，並傳回下載對應 .cab 檔案的位置。

## <a name="syntax"></a>語法


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrFileUrl* \[在\]
</dt> <dd>

要檢查之 ActiveX 物件的 URL。

</dd> <dt>

*bstrApprovedFileName* \[擴展\]
</dt> <dd>

已下載與 ActiveX 物件相關聯之 .cab 檔案的檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](/windows/desktop/SecCrypto/common-hresult-values)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback 定義為1823E7BA-EC36-447a-9B2E-B4912E15AFE7<br/>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

