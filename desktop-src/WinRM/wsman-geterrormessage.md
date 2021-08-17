---
title: 'GetErrorMessage 方法 (WSManDisp .h) '
description: 傳回格式化的字串，其中包含錯誤號碼的文字。
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- GetErrorMessage 方法 Windows 遠端管理
- GetErrorMessage 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，GetErrorMessage 方法
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e7f23a5d2678d3df024c78397aaeb6a388d8b75368f329867f6457b9ad4d84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742088"
---
# <a name="wsmangeterrormessage-method"></a>WSMan. GetErrorMessage 方法

傳回格式化的字串，其中包含錯誤號碼的文字。 這個方法會執行與 **Winrm** 命令列 **winrm helpmsg** *decimal 或十六進位錯誤號碼* 相同的操作。

## <a name="syntax"></a>語法


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*errorNumber* \[在\]
</dt> <dd>

來自 WinRM、WinHTTP 或其他作業系統元件之十進位或十六進位的錯誤訊息編號。

</dd> <dt>

*errorMessage* \[擴展\]
</dt> <dd>

格式化為 **Winrm** 命令所傳回之訊息的錯誤訊息字串。

</dd> </dl>

## <a name="remarks"></a>備註

對應的 c + + 方法是 [**IWSManEx：： GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 





