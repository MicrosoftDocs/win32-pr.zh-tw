---
description: 由檔案管理員延伸模組傳送，以抓取具有輸入焦點的 [檔案管理員] 視窗類型。
title: 'FM_GETFOCUS 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: 7512595008ad79d33bf1ac9b381b63831977282b83a8ce595c3d2689087c869c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459108"
---
# <a name="fm_getfocus-message"></a>FM \_ GETFOCUS 訊息

由檔案管理員延伸模組傳送，以抓取具有輸入焦點的 [檔案管理員] 視窗類型。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回具有輸入焦點的 [檔案管理員] 視窗類型。 它可以是下列值之一。



| 傳回碼                                                                                    | Description                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**FMFOCUS \_ 目錄**</dt> </dl>    | 目錄視窗的目錄部分。<br/> |
| <dl> <dt>**FMFOCUS \_ 樹狀結構**</dt> </dl>   | 目錄視窗的樹狀結構部分。<br/>      |
| <dl> <dt>**FMFOCUS \_ 磁片磁碟機**</dt> </dl> | 目錄視窗的磁片磁碟機列。<br/>         |
| <dl> <dt>**FMFOCUS \_ 搜尋**</dt> </dl> | 搜尋結果視窗。<br/>                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



 

 




