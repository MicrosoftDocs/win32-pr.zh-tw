---
description: SelectDefaultAudioLanguage 方法會設定 MSWebDVD 物件中目前的預設音訊語言。
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: SelectDefaultAudioLanguage 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509980"
---
# <a name="selectdefaultaudiolanguage-method"></a>SelectDefaultAudioLanguage 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`SelectDefaultAudioLanguage`方法會在 MSWebDVD 物件中設定目前的預設音訊語言。

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*
</dt> <dd>

將語言指定為整數 LCID 值。

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

將 DVD-音訊語言延伸模組指定為整數值。



| 值 | 描述       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | 標題          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSWebDVD 物件](mswebdvd-object.md)
</dt> </dl>

 

 



