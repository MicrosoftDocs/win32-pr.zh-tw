---
description: IsSubpictureStreamEnabled 方法會抓取值，指出目前的標題中是否已啟用指定的子圖片資料流程。
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: IsSubpictureStreamEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846640"
---
# <a name="issubpicturestreamenabled-method"></a>IsSubpictureStreamEnabled 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`IsSubpictureStreamEnabled`方法會抓取值，指出目前的標題中是否已啟用指定的子圖片資料流程。

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

將子圖片資料流程指定為整數。



| 值   | 描述              |
|---------|--------------------------|
| 0到31 | 子圖片資料流程        |
| 63      | 靜音低位元速率串流 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回布林值，指出指定的音訊資料流程是否可在目前的標題中使用。 True 表示它可供使用。

## <a name="remarks"></a>備註

雖然光碟最多可包含32子圖片串流，但每個標題都不一定會有每個資料流程。 在設定 [**CurrentSubpictureStream**](currentsubpicturestream-property.md) 屬性之前，請務必先確認是否有標題可用的資料流程。

 

 



