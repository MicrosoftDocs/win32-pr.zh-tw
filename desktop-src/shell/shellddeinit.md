---
description: 在目前的進程中註冊 Shell 動態資料交換 (DDE) 服務，通知系統目前的進程希望裝載 DDE 物件。
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: ShellDDEInit 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973593"
---
# <a name="shellddeinit-function"></a>ShellDDEInit 函式

在目前的進程中註冊 Shell 動態資料交換 (DDE) 服務，通知系統目前的進程希望裝載 DDE 物件。

## <a name="syntax"></a>語法


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*init* \[在\]
</dt> <dd>

類型： **BOOL**

**TRUE** 表示將目前的進程註冊為 DDE 主機; **FALSE** 表示將其取消註冊。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

呼叫此函式的進程會作為 Shell，並用來查看以 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ' open ' 動詞開啟之資料夾的內容。

此函式沒有相關聯的標頭或程式庫檔案，因此必須由序數值來呼叫。 使用 (Shdocvw.dll) 的 DLL 名稱呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。 然後使用該模組控制碼呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，並使用函式序號118來取得函式的位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows XP、Windows 2000 Professional \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shdocvw.dll (6.0 版或更新版本) </dt> </dl> |



 

 
