---
title: IDWriteFont2 IsColorFont 方法
description: 可判斷是否有可能需要色彩轉譯路徑。
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- IsColorFont 方法直接寫入
- IsColorFont 方法 Direct Write，IDWriteFont2 介面
- IDWriteFont2 介面 Direct Write，IsColorFont 方法
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384922"
---
# <a name="idwritefont2iscolorfont-method"></a>IDWriteFont2：： IsColorFont 方法

可判斷是否有可能需要色彩轉譯路徑。

## <a name="syntax"></a>語法


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **BOOL**

如果字型有 (COLR 和 CPAL 資料表的色彩資訊，則傳回 **TRUE** ，) ;否則 **為 FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                          |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





