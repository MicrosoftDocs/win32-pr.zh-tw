---
title: 色彩空間類型識別碼
description: 這些常數會指定 Postscript 2 色彩空間陣列的類型。 下列值是有效的色彩空間陣列類型。
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/02/2021
ms.locfileid: "106988511"
---
# <a name="color-space-type-identifiers"></a>色彩空間類型識別碼

這些常數會指定 Postscript 2 色彩空間陣列的類型。 下列值是有效的色彩空間陣列類型。

<dl> <dt>

<span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**
</dt> <dd> <dl> <dt>



從單色設定檔取得 CIEBasedA 色彩空間陣列。


</dt> </dl> </dd> <dt>

<span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA \_ 灰色**
</dt> <dd> <dl> <dt>



從單色設定檔取得 CIEBasedA 色彩空間陣列。


</dt> </dl> </dd> <dt>

<span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_ ABC**
</dt> <dd> <dl> <dt>



從 RGB 或 L <sup>\*</sup> a b 設定檔取得 CIEBasedABC 色彩空間陣列 <sup>\*</sup> 。


</dt> </dl> </dd> <dt>

<span id="CSA_DEF"></span><span id="csa_def"></span>**CSA \_ DEF**
</dt> <dd> <dl> <dt>



從 RGB 或 L <sup>\*</sup> a b 設定檔取得 CIEBasedDEF 色彩空間陣列 <sup>\*</sup> 。


</dt> </dl> </dd> <dt>

<span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA \_ RGB**
</dt> <dd> <dl> <dt>



從 RGB 設定檔取得 CIEBasedDEF 色彩空間陣列，後面接著 CIEBasedABC 色彩空間陣列。 執行時，如果印表機不支援 CIEBasedDEF 色彩空間，此函數會使用 CIEBasedABC 定義。


</dt> </dl> </dd> <dt>

<span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA \_ 實驗室**
</dt> <dd> <dl> <dt>



從 L <sup>\*</sup> a b 設定檔取得 CIEBasedABC 色彩空間陣列 <sup>\*</sup> 。


</dt> </dl> </dd> <dt>

<span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA \_ DEFG**
</dt> <dd> <dl> <dt>



從 CMYK 設定檔取得 CIEBasedDEFG 色彩空間陣列。


</dt> </dl> </dd> <dt>

<span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ CMYK**
</dt> <dd> <dl> <dt>



從 CMYK 設定檔取得 CIEBasedCMYK 色彩空間陣列。


</dt> </dl> </dd> </dl>

## <a name="see-also"></a>另請參閱

<dl> <dt>

[基本色彩管理概念](basic-color-management-concepts.md)
</dt> <dt>

[ICM 常數](wcs-constants.md)
</dt> </dl>

 

 




