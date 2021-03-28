---
description: 當使用者選擇 [檔案] 功能表中的 [取消刪除] 命令時，指定由 [檔案管理員] 呼叫的應用程式定義回呼函數。
title: 'FM_UNDELETE_PROC 函式指標 (Wfext) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194801"
---
# <a name="fm_undelete_proc-function-pointer"></a>FM 取消 \_ 刪除進程函式 \_ 指標

當使用者選擇 [檔案] 功能表中的 [取消 **刪除** ] 命令時，指定 **由 [檔** 管理器] 呼叫的應用程式定義回呼函數。

## <a name="syntax"></a>語法


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndOwner* 
</dt> <dd>

類型： **HWND**

檔案管理員的視窗控制碼。 取消刪除 DLL 應使用這個控制碼來指定 DLL 可能顯示之任何對話方塊或訊息方塊的擁有者視窗。

</dd> <dt>

*lpszDir* 
</dt> <dd>

類型： **LPSTR**

以 null 終止之字串的位址，其中包含初始目錄的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **DWORD**

傳回下列其中一個值。



| 傳回碼                                                                             | Description                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**-1**</dt> </dl>       | 發生錯誤。<br/>                                      |
| <dl> <dt>**IDOK**</dt> </dl>     | 已取消刪除檔案。 [檔案管理員] 會重新繪製其視窗。<br/> |
| <dl> <dt>**IDCANCEL**</dt> </dl> | 未刪除任何檔案。<br/>                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



 

 




