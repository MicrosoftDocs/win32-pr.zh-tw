---
description: 為您的應用程式保存的所有設定檔設定持續性群組識別碼清單。
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: 'WFDDisplaySinkSetPersistedGroupIDList 函式 (Wfdsink) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976804"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a>WFDDisplaySinkSetPersistedGroupIDList 函式

為您的應用程式保存的所有設定檔設定持續性群組識別碼清單。 您的應用程式在每次新增或刪除其儲存體中的設定檔時，都應該呼叫這個方法。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cGroupIDList* \[在\]
</dt> <dd>

*PGroupIDList* 指向的群組識別碼計數。

</dd> <dt>

*pGroupIDList* \[在\]
</dt> <dd>

*CGroupIDList* 群組識別碼陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

## <a name="remarks"></a>備註

一律會使用整個清單來呼叫這個方法，而非子集。 當設定檔存放區是空的時，可以使用0設定檔來呼叫此方法。

不屬於所提供清單的群組識別碼重新叫用將會失敗，並出現「失敗;未知的 P2P 群組」 (狀態 8) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows 10<br/>                                                                      |
| 伺服器支援結束<br/>    | Windows Server 2016<br/>                                                             |
| 標頭<br/>                   | <dl> <dt>Wfdsink。h</dt> </dl>       |
| 程式庫<br/>                  | <dl> <dt>Wifidisplay .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




