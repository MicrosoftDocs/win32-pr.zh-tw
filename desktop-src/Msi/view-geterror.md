---
description: View 物件的 GetError 方法會傳回發生錯誤的驗證錯誤和資料行名稱。
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ddbed26565598ad58b3605b7c70a9a5bbede3e5282ff4a7fa011df5c56bd8b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038798"
---
# <a name="viewgeterror-method"></a>GetError 方法

[**View**](view-object.md)物件的 **GetError** 方法會傳回發生錯誤的驗證錯誤和資料行名稱。 在自動化中，傳回的值為 ColumnName 形式的字串 \# \# ，其中 \# \# 代表2位數的錯誤碼。 它會傳回視圖錯誤陣列中的第一個錯誤;後續呼叫會傳回錯誤陣列中的下一個值。 一旦傳回 ' 00 ' 的值，就不會有其他錯誤存在，而且後續的呼叫只會再次迴圈執行陣列。

## <a name="syntax"></a>語法


```JScript
View.GetError()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




