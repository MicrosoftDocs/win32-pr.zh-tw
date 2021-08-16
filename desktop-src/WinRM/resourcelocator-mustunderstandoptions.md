---
title: 'ResourceLocator. MustUnderstandOptions 屬性 (WSManDisp .h) '
description: 取得或設定 ResourceLocator 物件的 MustUnderstandOptions 值。
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- MustUnderstandOptions 屬性 Windows 遠端管理
- MustUnderstandOptions 屬性 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理、MustUnderstandOptions 屬性
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a49c3af0372553c221dae902a5fdca0e026bb874f612b8e21f41e6a6870f7ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323736"
---
# <a name="resourcelocatormustunderstandoptions-property"></a>ResourceLocator. MustUnderstandOptions 屬性

取得或設定 [**ResourceLocator**](resourcelocator.md)物件的 **MustUnderstandOptions** 值。 您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a>屬性值

指出若為 **True**，則如果執行 [WS-Management 通訊協定](ws-management-protocol.md) 的服務無法處理選項，則必須傳回錯誤。

## <a name="remarks"></a>備註

**IWSManResourceLocator：： MustUnderstandOptions** 是對應的 c + + 屬性。

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





