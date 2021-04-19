---
description: 在 Windows Vista 和更新版本上，您可以使用虛擬地區設定來測試應用程式的可當地語系化性。 本主題包含使用虛擬程式碼的程式。
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: 使用虛擬地區設定進行當地語系化測試
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981880"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a><span data-ttu-id="e63ae-104">使用虛擬地區設定進行當地語系化測試</span><span class="sxs-lookup"><span data-stu-id="e63ae-104">Using pseudo-locales for localizability testing</span></span>

<span data-ttu-id="e63ae-105">[虛擬地區設定](pseudo-locales.md) 內建于 Windows Vista 和更新版本，因此您可以透過 (NLS) Api 的國家語言支援來存取它們。</span><span class="sxs-lookup"><span data-stu-id="e63ae-105">[Pseudo-locales](pseudo-locales.md) are built in to Windows Vista and later, so that you can access them via National Language Support (NLS) APIs.</span></span> <span data-ttu-id="e63ae-106">您可以使用虛擬地區設定來測試應用程式的可 [當地語系化](/windows/uwp/design/globalizing/globalizing-portal) 性。</span><span class="sxs-lookup"><span data-stu-id="e63ae-106">You can use pseudo-locales to test the [localizability](/windows/uwp/design/globalizing/globalizing-portal) of your applications.</span></span> <span data-ttu-id="e63ae-107">本主題包含使用虛擬程式碼的程式。</span><span class="sxs-lookup"><span data-stu-id="e63ae-107">This topic includes procedures for using pseudo-codes.</span></span>

> [!NOTE]
> <span data-ttu-id="e63ae-108">在虛擬地區設定中，需要特別考慮的一項工作就是列舉它們;不論是在您的程式碼中，或是在主控台的地區和語言選項部分中。</span><span class="sxs-lookup"><span data-stu-id="e63ae-108">One task that needs special consideration when it comes to pseudo-locales is enumerating them; whether in your code, or in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="e63ae-109">本主題稍後將詳細說明。</span><span class="sxs-lookup"><span data-stu-id="e63ae-109">More on that later in this topic.</span></span>

<span data-ttu-id="e63ae-110">虛擬地區設定的名稱為 "qps-qps-ploc"、"qps-ploca" 和 "qps-plocm"。</span><span class="sxs-lookup"><span data-stu-id="e63ae-110">The names of the pseudo-locales are "qps-ploc", "qps-ploca", and "qps-plocm".</span></span> <span data-ttu-id="e63ae-111">從 Windows 10，虛擬地區設定 "qps-Latn-x-sh" 也可供使用。</span><span class="sxs-lookup"><span data-stu-id="e63ae-111">As of Windows 10, the pseudo-locale "qps-Latn-x-sh" is also available.</span></span>

## <a name="retrieve-information-about-pseudo-locales"></a><span data-ttu-id="e63ae-112">取得虛擬地區設定的相關資訊</span><span class="sxs-lookup"><span data-stu-id="e63ae-112">Retrieve information about pseudo-locales</span></span>

<span data-ttu-id="e63ae-113">您可以使用 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 來取得虛擬地區設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e63ae-113">You can use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) to retrieve information about a pseudo-locale.</span></span> <span data-ttu-id="e63ae-114">將特定虛擬地區設定的名稱傳遞至函式 (查看上述) 的名稱清單。</span><span class="sxs-lookup"><span data-stu-id="e63ae-114">Pass into the function the name of the particular pseudo-locale (see the list of names above).</span></span> <span data-ttu-id="e63ae-115">例如，針對鏡像虛擬地區設定的 "qps-plocm"。</span><span class="sxs-lookup"><span data-stu-id="e63ae-115">For example, "qps-plocm" for the mirrored pseudo-locale.</span></span>

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a><span data-ttu-id="e63ae-116">搭配使用 LocaleNameToLCID 與虛擬地區設定</span><span class="sxs-lookup"><span data-stu-id="e63ae-116">Use LocaleNameToLCID with pseudo-locales</span></span>

<span data-ttu-id="e63ae-117">您可以使用虛擬地區設定的名稱來呼叫 NLS 對應函式 [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) 。</span><span class="sxs-lookup"><span data-stu-id="e63ae-117">You can call the NLS mapping function [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) with the name of a pseudo-locale.</span></span>

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a><span data-ttu-id="e63ae-118">啟用列舉的虛擬地區設定</span><span class="sxs-lookup"><span data-stu-id="e63ae-118">Enable pseudo-locales for enumeration</span></span>

<span data-ttu-id="e63ae-119">在您的應用程式中，您可以呼叫 [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) 來列舉系統識別的地區設定。</span><span class="sxs-lookup"><span data-stu-id="e63ae-119">In your application, you can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) to enumerate the locales that the system recognizes.</span></span> <span data-ttu-id="e63ae-120">主控台的 [地區及語言選項] 部分也會呼叫 **EnumSystemLocalesEx** 來建立所顯示的地區設定清單。</span><span class="sxs-lookup"><span data-stu-id="e63ae-120">The regional and language options portion of the Control Panel also calls **EnumSystemLocalesEx** to build the list of locales that it displays.</span></span> <span data-ttu-id="e63ae-121">不過，根據預設，系統不會辨識上面所列的四個虛擬地區設定，因此 **EnumSystemLocalesEx** 不會傳回它們。</span><span class="sxs-lookup"><span data-stu-id="e63ae-121">However, by default, the four pseudo-locales listed above are not recognized by the system, so they won't be returned by **EnumSystemLocalesEx**.</span></span> <span data-ttu-id="e63ae-122">針對 Windows Vista （含）以上的系統（包括 Windows 10 1709 版），解決方案是藉由將金鑰新增至 Windows 登錄來啟用虛擬地區設定。</span><span class="sxs-lookup"><span data-stu-id="e63ae-122">For systems from Windows Vista up to and including Windows 10, version 1709, the solution is to enable pseudo-locales by adding keys to the Windows Registry.</span></span>

<span data-ttu-id="e63ae-123">您可以在 HKEY \_ LOCAL \_ MACHINE \\ system \\ CurrentControlSet \\ Control \\ Nls 金鑰下，針對作業系統上安裝的語言來進行編輯。</span><span class="sxs-lookup"><span data-stu-id="e63ae-123">The edits are made under the HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Nls key for the languages installed on the operating system.</span></span> <span data-ttu-id="e63ae-124">您可以進行這些設定，以啟用虛擬地區設定。</span><span class="sxs-lookup"><span data-stu-id="e63ae-124">You can make these settings to enable the pseudo-locales.</span></span> <span data-ttu-id="e63ae-125">以下顯示的每個金鑰都是對應至所要啟用虛擬地區設定的十六進位 LCID。</span><span class="sxs-lookup"><span data-stu-id="e63ae-125">Each key shown below is the hexadecimal LCID corresponding to the pseudo-locale being enabled.</span></span> <span data-ttu-id="e63ae-126">每個值都是字串類型， (REG \_ SZ) 。</span><span class="sxs-lookup"><span data-stu-id="e63ae-126">Each value is of type string (REG\_SZ).</span></span>

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

<span data-ttu-id="e63ae-127">針對 Windows 10 版本1803，像這樣編輯 Windows 登錄沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="e63ae-127">For Windows 10, version 1803, editing the Windows Registry like this has no effect.</span></span> <span data-ttu-id="e63ae-128">但是您仍然可以使用虛擬地區設定的名稱來呼叫非列舉 NLS Api (請參閱上述的程式碼範例) ，以 (UI) 填入您的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="e63ae-128">But you can still call the non-enumerating NLS APIs with the names of the pseudo-locales (see the code examples above) to populate your user interface (UI).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e63ae-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="e63ae-129">Related topics</span></span>

* [<span data-ttu-id="e63ae-130">使用國家語言支援</span><span class="sxs-lookup"><span data-stu-id="e63ae-130">Using National Language Support</span></span>](using-national-language-support.md)
* [<span data-ttu-id="e63ae-131">虛擬地區設定</span><span class="sxs-lookup"><span data-stu-id="e63ae-131">Pseudo-Locales</span></span>](pseudo-locales.md)
* [<span data-ttu-id="e63ae-132">EnumSystemLocalesEx</span><span class="sxs-lookup"><span data-stu-id="e63ae-132">EnumSystemLocalesEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [<span data-ttu-id="e63ae-133">GetLocaleInfoEx</span><span class="sxs-lookup"><span data-stu-id="e63ae-133">GetLocaleInfoEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [<span data-ttu-id="e63ae-134">LocaleNameToLCID</span><span class="sxs-lookup"><span data-stu-id="e63ae-134">LocaleNameToLCID</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
