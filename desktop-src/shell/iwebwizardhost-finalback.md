---
description: 在主控伺服器端 HTML 頁面的頁面上，直接流覽至用戶端頁面。
title: 'WebWizardHost. FinalBack 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: 0338b20023fda059a5205c9a42a7b7d669c5554d5fca878fcb8904c807ceceae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092605"
---
# <a name="webwizardhostfinalback-method"></a>WebWizardHost. FinalBack 方法

在主控伺服器端 HTML 頁面的頁面上，直接流覽至用戶端頁面。

## <a name="syntax"></a>語法


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="remarks"></a>備註

當 wizard 顯示第一個伺服器端頁面，而且使用者按下 [ **上一步** ] 按鈕時，伺服器會在用戶端的事件處理常式收到該事件的通知時叫用 **FinalBack** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl> |



 

 




