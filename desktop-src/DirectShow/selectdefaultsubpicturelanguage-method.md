---
description: SelectDefaultSubpictureLanguage 方法會在 MSWebDVD 物件中設定目前的預設子圖片語言。
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: SelectDefaultSubpictureLanguage 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aaa6b927d33626299258ac54136e1a67b0dedb40427a35d9c79465be3e9a15d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072582"
---
# <a name="selectdefaultsubpicturelanguage-method"></a>SelectDefaultSubpictureLanguage 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`SelectDefaultSubpictureLanguage`方法會在 **MSWebDVD** 物件中設定目前的預設子圖片語言。

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*
</dt> <dd>

將語言指定為整數。

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

將子圖片語言延伸模組指定為整數。



| 值 | 描述                    |
|-------|--------------------------------|
| 0     | 未指定擴充功能        |
| 1     | 一般字幕                |
| 2     | 大標題                   |
| 3     | 子女的標題            |
| 5     | 一般隱藏式輔助字幕         |
| 6     | 大型隱藏式輔助字幕            |
| 7     | 兒童隱藏式輔助字幕     |
| 9     | Forced                         |
| 13    | 一般導演的留言     |
| 14    | 大型總監的評論        |
| 15    | 子女的 Director's 批註 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

子圖片語言延伸模組提供有關子圖片的進一步資訊。

 

 



