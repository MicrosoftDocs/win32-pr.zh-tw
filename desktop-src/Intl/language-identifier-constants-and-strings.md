---
description: 每個語言識別項都是由主要語言識別項所組成，指出語言和表示國家/地區的子語言識別項。
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: 語言識別項常數和字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319392"
---
# <a name="language-identifier-constants-and-strings"></a><span data-ttu-id="36351-103">語言識別項常數和字串</span><span class="sxs-lookup"><span data-stu-id="36351-103">Language Identifier Constants and Strings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36351-104">語言識別項常數已被取代，因此不建議使用。</span><span class="sxs-lookup"><span data-stu-id="36351-104">Language identifier constants are deprecated and their use is discouraged.</span></span> <span data-ttu-id="36351-105">最好是使用地區設定名稱，而非地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="36351-105">Use of locale names instead of locale identifiers is always preferable.</span></span>

<span data-ttu-id="36351-106">如需語言識別項的描述，請參閱 [語言識別項](language-identifiers.md) 。</span><span class="sxs-lookup"><span data-stu-id="36351-106">See [language identifier](language-identifiers.md) for a description of language identifiers.</span></span>

<span data-ttu-id="36351-107">主要或子語言識別項可以是使用者定義的或預先定義的識別碼。</span><span class="sxs-lookup"><span data-stu-id="36351-107">A primary or sublanguage identifier can be user-defined or predefined.</span></span> <span data-ttu-id="36351-108">如需預先定義的主要語言識別項及其有效的語言識別項，請參閱 [[MS-LCID]： Windows 語言代碼識別碼 (LCID) 參考](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f)。</span><span class="sxs-lookup"><span data-stu-id="36351-108">For the predefined primary language identifiers with their valid sublanguage identifiers, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span></span>

> [!Note]  
> <span data-ttu-id="36351-109">如果沒有與主要語言識別項搭配使用的語言識別項，您的應用程式應該使用 **SUBLANG \_ 預設值**。</span><span class="sxs-lookup"><span data-stu-id="36351-109">If there is no sublanguage identifier to use with a primary language identifier, your application should use **SUBLANG\_DEFAULT**.</span></span> <span data-ttu-id="36351-110">針對所有主要語言的 sublanguages，它應該使用 **SUBLANG \_ 中立** 的資源。</span><span class="sxs-lookup"><span data-stu-id="36351-110">It should use **SUBLANG\_NEUTRAL** for resources that are the same for all sublanguages of a primary language.</span></span>

<span data-ttu-id="36351-111">使用者定義的主要語言識別項具有範圍0x0200 至0x03ff 的值。</span><span class="sxs-lookup"><span data-stu-id="36351-111">A user-defined primary language identifier has a value in the range 0x0200 to 0x03ff.</span></span> <span data-ttu-id="36351-112">所有其他值則保留供作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="36351-112">All other values are reserved for operating system use.</span></span>

<span data-ttu-id="36351-113">使用者定義的子語言識別項具有範圍0x20 到0x3f 的值。</span><span class="sxs-lookup"><span data-stu-id="36351-113">A user-defined sublanguage identifier has a value in the range 0x20 to 0x3f.</span></span> <span data-ttu-id="36351-114">所有其他值則保留供作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="36351-114">All other values are reserved for operating system use.</span></span>
