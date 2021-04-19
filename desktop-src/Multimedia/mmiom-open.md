---
title: 'MMIOM_OPEN 訊息 (Mmsystem .h) '
description: MMIOM \_ 開啟的訊息會由 mmioOpen 函數傳送至 i/o 程式，以要求開啟或刪除檔案。
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- MMIOM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106972702"
---
# <a name="mmiom_open-message"></a>MMIOM \_ 開啟的訊息

**MMIOM \_ 開啟** 的訊息會由 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)函數傳送至 i/o 程式，以要求開啟或刪除檔案。


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*
</dt> <dd>

以 Null 終止的字串，其中包含要開啟的檔案名。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

保留的。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 MMSYSERR \_ >aad-userreadusingalternativesecurityid-noerror，否則會傳回錯誤。 可能的錯誤值包括下列各項：



| 需求 | 值 |
|--------------------|---------------------------------------------|
| MMIOM \_ CANNOTOPEN  | 無法開啟檔案。               |
| MMIOM \_ OUTOFMEMORY | 記憶體不足，無法執行此作業。 |



 

## <a name="remarks"></a>備註

[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構的 **dwFlags** 成員包含傳遞至 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)函數的旗標。

[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構的 **lDiskOffset** 成員會初始化為零。 如果這個值不正確，i/o 程式必須更正它。

如果應用程式將 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) 結構傳遞給 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)，則傳回值會在 **wErrorRet** 成員中傳回。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



 

