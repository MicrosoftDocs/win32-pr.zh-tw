---
title: 'ResourceLocator. ClearSelectors 方法 (WSManDisp .h) '
description: 從 ResourceLocator 物件移除所有選取器。
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- ClearSelectors 方法 Windows 遠端管理
- ClearSelectors 方法 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理，ClearSelectors 方法
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5dbf1322a5e0c36a1383581e2822fbd00a00e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105629"
---
# <a name="resourcelocatorclearselectors-method"></a>ResourceLocator. ClearSelectors 方法

從 [**ResourceLocator**](resourcelocator.md)物件移除所有 [*選取器*](windows-remote-management-glossary.md)。 您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。

## <a name="syntax"></a>語法


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="remarks"></a>備註

**IWSManResourceLocator：： ClearSelectors** 是對應的 c + + 方法。

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





