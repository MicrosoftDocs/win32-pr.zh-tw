---
description: 流覽至裝載伺服器端 HTML 頁面的頁面下的用戶端 wizard 頁面，或者，如果沒有進一步的用戶端頁面，則完成 wizard。
title: 'WebWizardHost. FinalNext 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: a694ced28663a005bfdacd406adb3f6b3d6cd0300db2a101c9fdee4bf215a23d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821118"
---
# <a name="webwizardhostfinalnext-method"></a>WebWizardHost. FinalNext 方法

流覽至裝載伺服器端 HTML 頁面的頁面下的用戶端 wizard 頁面，或者，如果沒有進一步的用戶端頁面，則完成 wizard。

## <a name="syntax"></a>語法


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="remarks"></a>備註

當 wizard 顯示最後一個伺服器端 HTML 網頁，而且使用者按 **下 [下一步** **] 或 [完成]** 按鈕時，伺服器會在該按鈕的事件處理常式中叫用 **FinalNext** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl> |



 

 




