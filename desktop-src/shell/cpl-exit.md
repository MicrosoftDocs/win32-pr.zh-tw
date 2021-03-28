---
description: 先傳送一次至主控台應用程式的 CPlApplet 函式，再釋放包含主控台應用程式的 DLL。
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: 'CPL_EXIT 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191179"
---
# <a name="cpl_exit-message"></a>CPL 結束 \_ 訊息

先傳送一次至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式，再釋放包含主控台應用程式的 DLL。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式成功處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

這則訊息會在傳送最後一個 [**CPL \_ 停止**](cpl-stop.md) 訊息之後傳送。

為了回應這則訊息，主控台的應用程式必須釋放已配置的記憶體，並執行全域層級的清除。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Cpl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
