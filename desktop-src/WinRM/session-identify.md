---
title: Session)  (WSManDisp 的方法
description: 查詢遠端電腦，以判斷它是否支援 WS-Management 的通訊協定。
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- 識別方法 Windows 遠端管理
- 識別方法 Windows 遠端管理、會話物件
- 會話物件 Windows 遠端管理，識別方法
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968591"
---
# <a name="sessionidentify-method"></a>Session。識別方法

**會話。識別** 方法會查詢遠端電腦，以判斷它是否支援 WS-Management 的通訊協定。 如需詳細資訊，請參閱偵測 [遠端電腦是否支援 WS-Management 的通訊協定](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)。

## <a name="syntax"></a>語法


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在中，選擇性\]
</dt> <dd>

若要在經過驗證的模式下傳送要求，請使用來自 **WSManSessionFlags** 列舉的驗證常數。 若要以未驗證的模式傳送，請使用 **WSManFlagUseNoAuthentication**。 如需詳細資訊，請參閱 [**驗證常數**](authentication-constants.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

XML 字串，這個字串會指定 WS-Management 的通訊協定版本、作業系統廠商，以及要求是否已通過驗證的作業系統版本。

## <a name="remarks"></a>備註

**會話。識別** 是以定義為 wsmanIdentity 的 [WS-Management 通訊協定](ws-management-protocol.md) 作業為基礎。 這是在 SOAP 封包中指定，如下所示：


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a>範例

下列 VBScript 範例會將未經驗證的識別要求傳送到相同網域中名為 Remote 的遠端電腦。


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**工作階段**](session.md)
</dt> <dt>

[**Iwsmansession.invoke：：識別**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[WS-Management 通訊協定](ws-management-protocol.md)
</dt> </dl>

 

 





