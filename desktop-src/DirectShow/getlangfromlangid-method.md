---
description: GetLangFromLangID 方法會在指定主要語言識別項時，抓取人們可讀取的字串。
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: GetLangFromLangID 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846315"
---
# <a name="getlangfromlangid-method"></a>GetLangFromLangID 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`GetLangFromLangID`當指定主要語言識別項時，方法會抓取人們可讀取的字串。

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*
</dt> <dd>

將主要語言識別項指定為整數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回可在應用程式的使用者介面中顯示之語言的字串表示。

## <a name="remarks"></a>備註

雖然此方法已命名 `GetLangFromLangID` ，但您傳遞的參數實際上是主要語言識別項，而不是語言識別項。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> <dt>

[**GetDVDTextLanguageLCID**](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



