---
description: IsAudioStreamEnabled 方法會抓取值，指出目前的標題中是否已啟用指定的音訊資料流程。
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: IsAudioStreamEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2131376346f2a0311fc5acd8e0051292a12fb0145b44226363c7d891a5ef3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817473"
---
# <a name="isaudiostreamenabled-method"></a>IsAudioStreamEnabled 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`IsAudioStreamEnabled`方法會抓取值，指出目前的標題中是否已啟用指定的音訊資料流程。

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

將音訊串流指定為0到7的整數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回布林值，指出指定的音訊資料流程是否適用于目前的標題。 True 表示它可供使用。

## <a name="remarks"></a>備註

雖然光碟最多可包含八個獨立的音訊串流，但每個標題都不一定會有每個資料流程。 例如，主要電影標題可能有三個英文、西班牙文和日文音訊串流，但 "景點" 標題可能只有一個英文的音訊串流。 在設定 [**CurrentAudioStream**](currentaudiostream-property.md) 屬性之前，請務必先確認是否有標題可用的資料流程。

 

 



