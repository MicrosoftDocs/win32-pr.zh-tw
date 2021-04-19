---
description: 地區設定 \_ 自訂 \* 常數
ms.assetid: a41a7f55-8905-47a1-86c3-74ed40b3834c
title: LOCALE_CUSTOM * 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4e02cc672241fd609a5eda975c0e9e13d29908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972161"
---
# <a name="locale_custom-constants"></a><span data-ttu-id="18a6a-103">地區設定 \_ 自訂 \* 常數</span><span class="sxs-lookup"><span data-stu-id="18a6a-103">LOCALE\_CUSTOM\* Constants</span></span>

<span data-ttu-id="18a6a-104">本主題定義 \_ \* NLS 用來表示 [自訂地區](custom-locales.md)設定的地區設定自訂常數。</span><span class="sxs-lookup"><span data-stu-id="18a6a-104">This topic defines the LOCALE\_CUSTOM\* constants used by NLS to represent [custom locales](custom-locales.md).</span></span>



| <span data-ttu-id="18a6a-105">值</span><span class="sxs-lookup"><span data-stu-id="18a6a-105">Value</span></span>                       | <span data-ttu-id="18a6a-106">意義</span><span class="sxs-lookup"><span data-stu-id="18a6a-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a6a-107">地區設定 \_ 自訂 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="18a6a-107">LOCALE\_CUSTOM\_DEFAULT</span></span>     | <span data-ttu-id="18a6a-108">**Windows Vista 和更新版本：** 預設的自訂地區設定。</span><span class="sxs-lookup"><span data-stu-id="18a6a-108">**Windows Vista and later:** The default custom locale.</span></span> <span data-ttu-id="18a6a-109">當 NLS 函數必須針對目前使用者的 [補充地區](custom-locales.md) 設定傳回地區設定識別碼時，此函式會傳回此值，而不是 [地區設定 \_ 使用者 \_ 預設](locale-user-default.md)值。</span><span class="sxs-lookup"><span data-stu-id="18a6a-109">When an NLS function must return a locale identifier for a [supplemental locale](custom-locales.md) for the current user, the function returns this value instead of [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span> <span data-ttu-id="18a6a-110">地區設定 \_ 自訂 \_ 預設值為0x0C00。</span><span class="sxs-lookup"><span data-stu-id="18a6a-110">The value of LOCALE\_CUSTOM\_DEFAULT is 0x0C00.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="18a6a-111">地區設定 \_ 自訂 \_ UI \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="18a6a-111">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span> | <span data-ttu-id="18a6a-112">**Windows Vista 和更新版本：** MUI 的預設自訂地區設定。</span><span class="sxs-lookup"><span data-stu-id="18a6a-112">**Windows Vista and later:** The default custom locale for MUI.</span></span> <span data-ttu-id="18a6a-113">使用者慣用的 UI 語言和系統慣用 UI 語言最多可以包含一個由語言介面套件 (LIP) 所執行的單一語言，而且語言識別項會對應至補充地區設定。</span><span class="sxs-lookup"><span data-stu-id="18a6a-113">The user preferred UI languages and the system preferred UI languages can include at most a single language that is implemented by a Language Interface Pack (LIP) and for which the language identifier corresponds to a supplemental locale.</span></span> <span data-ttu-id="18a6a-114">如果清單中有這類語言，常數就會用來在特定內容中參考該語言。</span><span class="sxs-lookup"><span data-stu-id="18a6a-114">If there is such a language in a list, the constant is used to refer to that language in certain contexts.</span></span> <span data-ttu-id="18a6a-115">地區設定 \_ 自訂 \_ UI \_ 預設值為0x1400。</span><span class="sxs-lookup"><span data-stu-id="18a6a-115">The value of LOCALE\_CUSTOM\_UI\_DEFAULT is 0x1400.</span></span>                    |
| <span data-ttu-id="18a6a-116">未指定地區設定的 \_ 自訂 \_</span><span class="sxs-lookup"><span data-stu-id="18a6a-116">LOCALE\_CUSTOM\_UNSPECIFIED</span></span> | <span data-ttu-id="18a6a-117">**Windows Vista 和更新版本：** 未指定的自訂地區設定，用來識別目前使用者的地區設定以外的所有補充地區設定。</span><span class="sxs-lookup"><span data-stu-id="18a6a-117">**Windows Vista and later:** An unspecified custom locale, used to identify all supplemental locales except the locale for the current user.</span></span> <span data-ttu-id="18a6a-118">補充地區設定的地區設定識別碼無法彼此區別，但可依其 [地區設定名稱](locale-names.md)來區別。</span><span class="sxs-lookup"><span data-stu-id="18a6a-118">Supplemental locales cannot be distinguished from one another by their locale identifiers, but can be distinguished by their [locale names](locale-names.md).</span></span> <span data-ttu-id="18a6a-119">某些 NLS 函數可以傳回這個常數，表示它們無法針對特定地區設定提供有用的識別碼。</span><span class="sxs-lookup"><span data-stu-id="18a6a-119">Certain NLS functions can return this constant to indicate that they cannot provide a useful identifier for a particular locale.</span></span> <span data-ttu-id="18a6a-120">未指定地區設定的值 \_ \_ 為0x1000。</span><span class="sxs-lookup"><span data-stu-id="18a6a-120">The value of LOCALE\_CUSTOM\_UNSPECIFIED is 0x1000.</span></span> |



 

 

 



