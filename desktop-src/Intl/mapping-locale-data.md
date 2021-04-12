---
description: NLS 包含許多 API 函式，可讓您的應用程式用來對應地區設定識別碼與地區設定名稱之間的地區設定資料，以及列出中立的地區設定。
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: 對應地區設定資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191702"
---
# <a name="mapping-locale-data"></a><span data-ttu-id="5a3a2-103">對應地區設定資料</span><span class="sxs-lookup"><span data-stu-id="5a3a2-103">Mapping Locale Data</span></span>

<span data-ttu-id="5a3a2-104">NLS 包含許多 API 函式，可讓您的應用程式用來對應 [地區設定識別碼](locale-identifiers.md) 與 [地區設定名稱](locale-names.md)之間的地區設定資料，以及列出中立的地區設定。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-104">NLS includes a number of API functions that your applications can use to map locale data between [locale identifiers](locale-identifiers.md) and [locale names](locale-names.md), and list neutral locales.</span></span> <span data-ttu-id="5a3a2-105">本主題討論如何在 Windows Vista 和更新版本以及 Windows Vista 之前版本的作業系統上使用這些函式 (有時也稱為「下層系統」 ) 。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-105">This topic discusses the use of these functions on Windows Vista and later and on pre-Windows Vista operating systems (sometimes called "downlevel systems").</span></span>

## <a name="map-locale-data-on-windows-vista-and-later"></a><span data-ttu-id="5a3a2-106">在 Windows Vista 和更新版本上對應地區設定資料</span><span class="sxs-lookup"><span data-stu-id="5a3a2-106">Map Locale Data on Windows Vista and Later</span></span>

<span data-ttu-id="5a3a2-107">NLS 提供數個地區設定對應函式，可供您開發用來在 Windows Vista 和更新版本上執行的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-107">NLS provides several locale mapping functions for use by applications that you develop to run on Windows Vista and later.</span></span> <span data-ttu-id="5a3a2-108">它也包含您的應用程式可用來列舉中性地區設定的函式。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-108">It also includes functions that your applications can use to enumerate neutral locales.</span></span>

<span data-ttu-id="5a3a2-109">**使用標準轉換函數進行資料對應**</span><span class="sxs-lookup"><span data-stu-id="5a3a2-109">**Use the Standard Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="5a3a2-110">若要在地區設定名稱和地區設定識別碼之間進行對應，您的應用程式可以呼叫 [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) 函數。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-110">To map between a locale name and a locale identifier, your application can call the [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function.</span></span> <span data-ttu-id="5a3a2-111">應用程式會使用 [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) ，在地區設定識別碼和地區設定名稱之間進行對應。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-111">The application uses [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to map between a locale identifier and a locale name.</span></span>

<span data-ttu-id="5a3a2-112">**列出中性地區設定**</span><span class="sxs-lookup"><span data-stu-id="5a3a2-112">**List Neutral Locales**</span></span>

<span data-ttu-id="5a3a2-113">若要列舉 Windows 7 和更新版本的中性地區設定，您的應用程式可以呼叫 [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) ，並將 *DwFlags* 設定為 [**LOCALE \_ NEUTRALDATA**](locale-neutraldata.md)。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-113">To enumerate neutral locales for Windows 7 and later, your application can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) with *dwFlags* set to [**LOCALE\_NEUTRALDATA**](locale-neutraldata.md).</span></span> <span data-ttu-id="5a3a2-114">它也可以使用 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) ，並將 *LCType* 設定為 [**地區設定 \_ INEUTRAL**](locale-ineutral.md)。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-114">It can also use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with *LCType* set to [**LOCALE\_INEUTRAL**](locale-ineutral.md).</span></span>

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="5a3a2-115">在 Windows Vista 前版作業系統上對應地區設定資料</span><span class="sxs-lookup"><span data-stu-id="5a3a2-115">Map Locale Data on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="5a3a2-116">NLS 包含 (DLL) 的直接程式庫，可供您開發的應用程式在 Windows Vista 之前的作業系統上執行。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-116">NLS includes a direct-link library (DLL) to use for applications that you develop to run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="5a3a2-117">DLL 支援轉換和列出資料對應的函數。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-117">The DLL supports both conversion and listing functions for data mapping.</span></span>

> [!Note]  
> <span data-ttu-id="5a3a2-118">只在 Windows Vista 和更新版本上執行的應用程式不應使用下層對應或清單功能。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-118">Applications that only run on Windows Vista and later should not use the downlevel mapping or listing functions.</span></span>

 

<span data-ttu-id="5a3a2-119">**使用早期轉換函數進行資料對應**</span><span class="sxs-lookup"><span data-stu-id="5a3a2-119">**Use the Downlevel Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="5a3a2-120">以下層系統為目標的應用程式可以呼叫 [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) 函式，將地區設定識別碼轉換為地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-120">Your application targeted at a downlevel system can call the [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) function to convert a locale identifier to a locale name.</span></span> <span data-ttu-id="5a3a2-121">如果需要將地區設定名稱轉換成地區設定識別碼，則應該呼叫 [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md)。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-121">If it needs to convert a locale name to a locale identifier, it should call [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span></span>

<span data-ttu-id="5a3a2-122">**使用下層清單函式來列舉中性地區設定**</span><span class="sxs-lookup"><span data-stu-id="5a3a2-122">**Use the Downlevel Listing Functions to Enumerate Neutral Locales**</span></span>

<span data-ttu-id="5a3a2-123">您的應用程式應該呼叫 [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) ，以取得地區設定的父系地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-123">Your application should call the [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) to retrieve the locale identifier of the parent for a locale.</span></span> <span data-ttu-id="5a3a2-124">如果應用程式需要取得地區設定之父系的地區設定名稱，則應該呼叫 [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md)。</span><span class="sxs-lookup"><span data-stu-id="5a3a2-124">If the application needs to get the locale name of the parent for the locale, it should call [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a3a2-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a3a2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a3a2-126">使用國家語言支援</span><span class="sxs-lookup"><span data-stu-id="5a3a2-126">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="5a3a2-127">地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="5a3a2-127">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="5a3a2-128">地區設定名稱</span><span class="sxs-lookup"><span data-stu-id="5a3a2-128">Locale Names</span></span>](locale-names.md)
</dt> </dl>

 

 



