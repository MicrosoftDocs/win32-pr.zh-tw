---
title: 'ResourceLocator. AddSelector 方法 (WSManDisp .h) '
description: 將選取器加入至 ResourceLocator 物件。 選取器會指定資源的特定實例。
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- AddSelector 方法 Windows 遠端管理
- AddSelector 方法 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理，AddSelector 方法
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934424"
---
# <a name="resourcelocatoraddselector-method"></a>ResourceLocator. AddSelector 方法

將 [*選取器*](windows-remote-management-glossary.md) 加入至 [**ResourceLocator**](resourcelocator.md) 物件。 選取器會指定 *資源* 的特定實例。 您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。

## <a name="syntax"></a>語法


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*resourceSelName* \[在\]
</dt> <dd>

選取器名稱。 例如，在要求 WMI 資料時，此參數是 WMI 類別的索引鍵屬性。

</dd> <dt>

*selValue* \[在\]
</dt> <dd>

選取器的值。 例如，對於 WMI 資料而言，此參數包含識別特定實例之索引鍵屬性的值。

</dd> </dl>

## <a name="remarks"></a>備註

**IWSManResourceLocator：： AddSelector** 是對應的 c + + 方法。

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

 

 





