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
# <a name="getlangfromlangid-method"></a><span data-ttu-id="f7c7e-103">GetLangFromLangID 方法</span><span class="sxs-lookup"><span data-stu-id="f7c7e-103">GetLangFromLangID Method</span></span>

> [!Note]  
> <span data-ttu-id="f7c7e-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="f7c7e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f7c7e-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f7c7e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f7c7e-106">`GetLangFromLangID`當指定主要語言識別項時，方法會抓取人們可讀取的字串。</span><span class="sxs-lookup"><span data-stu-id="f7c7e-106">The `GetLangFromLangID` method retrieves a human-readable string when given a primary language ID.</span></span>

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a><span data-ttu-id="f7c7e-107">參數</span><span class="sxs-lookup"><span data-stu-id="f7c7e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7c7e-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span><span class="sxs-lookup"><span data-stu-id="f7c7e-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span></span>
</dt> <dd>

<span data-ttu-id="f7c7e-109">將主要語言識別項指定為整數。</span><span class="sxs-lookup"><span data-stu-id="f7c7e-109">Specifies the primary language ID as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7c7e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7c7e-110">Return Value</span></span>

<span data-ttu-id="f7c7e-111">傳回可在應用程式的使用者介面中顯示之語言的字串表示。</span><span class="sxs-lookup"><span data-stu-id="f7c7e-111">Returns a String representation of the language that can be displayed in the application's user interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7c7e-112">備註</span><span class="sxs-lookup"><span data-stu-id="f7c7e-112">Remarks</span></span>

<span data-ttu-id="f7c7e-113">雖然此方法已命名 `GetLangFromLangID` ，但您傳遞的參數實際上是主要語言識別項，而不是語言識別項。</span><span class="sxs-lookup"><span data-stu-id="f7c7e-113">Although this method is named `GetLangFromLangID`, the parameter that you pass is actually the primary language ID, not the language ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7c7e-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7c7e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c7e-115">**GetAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="f7c7e-115">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> <dt>

[<span data-ttu-id="f7c7e-116">**GetDVDTextLanguageLCID**</span><span class="sxs-lookup"><span data-stu-id="f7c7e-116">**GetDVDTextLanguageLCID**</span></span>](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



