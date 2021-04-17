---
description: GetDVDTextLanguageLCID 方法會針對指定的文字字串區塊，抓取 (LCID) 的地區設定識別碼。
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: GetDVDTextLanguageLCID 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509819"
---
# <a name="getdvdtextlanguagelcid-method"></a>GetDVDTextLanguageLCID 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`GetDVDTextLanguageLCID`方法會針對指定的文字字串區塊，抓取 (LCID) 的地區設定識別碼。

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

將光碟上的文字語言區塊指定為整數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 LCID 值，其中包含指定撰寫字串時所使用之語言的資訊。

## <a name="remarks"></a>備註

補充文字字串會儲存在光碟的連續區塊中。每種語言都有一個字串區塊。 應用程式會以索引指定這些區塊，而索引必須小於 [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md)傳回的值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSWebDVD 物件](mswebdvd-object.md)
</dt> <dt>

[**GetLangFromLangID**](getlangfromlangid-method.md)
</dt> </dl>

 

 



