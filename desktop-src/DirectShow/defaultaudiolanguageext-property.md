---
description: DefaultAudioLanguageExt 屬性會抓取預設的 DVD-音訊語言延伸模組。
ms.assetid: 628af2aa-e528-4689-953b-558e13e1d513
title: DefaultAudioLanguageExt 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5ce89099cd8e31cde9beb8bb3c8a9f1e16b3b0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509902"
---
# <a name="defaultaudiolanguageext-property"></a>DefaultAudioLanguageExt 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

屬性會抓取 `DefaultAudioLanguageExt` 預設的 DVD-音訊語言延伸模組。

``` syntax
[ iLangExt = ] MSWebDVD.DefaultAudioLanguageExt
```

## <a name="return-value"></a>傳回值

傳回表示預設音訊語言延伸模組的整數值。 如需可能的值，請參閱備註。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 下表顯示 DVD-音訊語言延伸模組的可能值。



| 值 | 描述       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | 標題          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

 

 



