---
description: GetSubpictureLanguage 方法會抓取指定之子圖片資料流程的語言。
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: GetSubpictureLanguage 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973535"
---
# <a name="getsubpicturelanguage-method"></a><span data-ttu-id="cf7a0-103">GetSubpictureLanguage 方法</span><span class="sxs-lookup"><span data-stu-id="cf7a0-103">GetSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="cf7a0-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="cf7a0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cf7a0-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="cf7a0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cf7a0-106">方法會抓取 `GetSubpictureLanguage` 指定之子圖片資料流程的語言。</span><span class="sxs-lookup"><span data-stu-id="cf7a0-106">The `GetSubpictureLanguage` method retrieves the language for the specified subpicture stream.</span></span>

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="cf7a0-107">參數</span><span class="sxs-lookup"><span data-stu-id="cf7a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf7a0-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="cf7a0-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="cf7a0-109">指定您想要取出其文字語言作為整數的子圖片資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="cf7a0-109">Specifies the subpicture stream number whose text language you want to retrieve as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf7a0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf7a0-110">Return Value</span></span>

<span data-ttu-id="cf7a0-111">傳回人們可讀取的字串，識別目前標題中音訊資料流程的語言。</span><span class="sxs-lookup"><span data-stu-id="cf7a0-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



