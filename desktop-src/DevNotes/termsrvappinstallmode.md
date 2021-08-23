---
description: 判斷終端機伺服器是否處於安裝模式。
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: TermsrvAppInstallMode 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f6bf6408fb7bd72b1757b8ca2219e1bbd2cc612829359fdcaf090786e8e7e98b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570888"
---
# <a name="termsrvappinstallmode-function"></a>TermsrvAppInstallMode 函式

\[這項功能不受支援，因此不應該使用。 它可能會在未事先通知的情況下，完全變更或消失。\]

判斷終端機伺服器是否處於安裝模式。

## <a name="syntax"></a>語法


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

如果終端機伺服器處於安裝模式，則此函式會傳回 **TRUE** ，如果是在執行模式，則會傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




