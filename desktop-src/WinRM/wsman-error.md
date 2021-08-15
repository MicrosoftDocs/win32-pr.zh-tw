---
title: 'WSMan. Error 屬性 (WSManDisp .h) '
description: 如果 Windows 遠端管理服務無法建立會話物件、ConnectionOptions 物件或 ResourceLocator 物件，請在 XML 資料流程中取得先前呼叫 WSMan 方法的其他錯誤資訊。
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Error 屬性 Windows 遠端管理
- Error 屬性 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，Error 屬性
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d72c99150d3c6ac95e91e6a9674ab6364e8ea46fabf3d58d50556e129933cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742193"
---
# <a name="wsmanerror-property"></a>WSMan. Error 屬性

如果 Windows 遠端管理服務無法建立 [**會話**](session.md)物件、 [**ConnectionOptions**](connectionoptions.md)物件或 [**ResourceLocator**](resourcelocator.md)物件，請在 XML 資料流程中取得先前呼叫 [**WSMan**](wsman.md)方法的其他錯誤資訊。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a>屬性值

錯誤資訊的 XML 標記法。

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

 

 





