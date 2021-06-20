---
description: 瞭解結構擴充性。 布建是以與裝置無關的方式和裝置特定的方式來擴充常數和結構。
ms.assetid: d30f80c3-3535-4d78-b0a1-c9a7389f8fd4
title: 結構擴充性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ec7e71154ad2550a595e59763bec3a25dd6f20a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403951"
---
# <a name="structure-extensibility"></a><span data-ttu-id="1577e-104">結構擴充性</span><span class="sxs-lookup"><span data-stu-id="1577e-104">Structure Extensibility</span></span>

<span data-ttu-id="1577e-105">布建是以與裝置無關的方式，以及裝置特定的 (廠商特定) 方式來擴充常數和結構。</span><span class="sxs-lookup"><span data-stu-id="1577e-105">Provisions are made for extending constants and structures both in a device-independent way and in a device-specific (vendor-specific) way.</span></span>

<span data-ttu-id="1577e-106">在純量列舉的常數中，會保留值範圍，供未來的一般延伸模組使用。</span><span class="sxs-lookup"><span data-stu-id="1577e-106">In constants that are scalar enumerations, a range of values is reserved for future common extensions.</span></span> <span data-ttu-id="1577e-107">其餘的值會識別為裝置特定。</span><span class="sxs-lookup"><span data-stu-id="1577e-107">The remainder of values is identified as device specific.</span></span> <span data-ttu-id="1577e-108">廠商可以用任何方式定義這些值的意義。</span><span class="sxs-lookup"><span data-stu-id="1577e-108">A vendor can define meanings for these values in any way.</span></span> <span data-ttu-id="1577e-109">這些值的解讀會以 [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)資料結構所提供的 *延伸模組識別碼* 做為索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1577e-109">The interpretation of these values is keyed to the *extension identifier* provided through the [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) data structure.</span></span> <span data-ttu-id="1577e-110">針對定義為位旗標的常數，會保留低序位位範圍，其中高序位位可以是擴充功能的特定範圍。</span><span class="sxs-lookup"><span data-stu-id="1577e-110">For constants that are defined as bit flags, a range of low-order bits are reserved, where the high-order bits can be extension specific.</span></span> <span data-ttu-id="1577e-111">建議將擴充值和位陣列使用最高值或高序位位的位。</span><span class="sxs-lookup"><span data-stu-id="1577e-111">It is recommended that extended values and bit arrays use bits from the highest value or high-order bit down.</span></span> <span data-ttu-id="1577e-112">如果未來需要這樣做，則可以選擇在一般部分和延伸部分之間移動框線。</span><span class="sxs-lookup"><span data-stu-id="1577e-112">This leaves the option to move the border between the common portion and extension portion if there is need to do so in the future.</span></span> <span data-ttu-id="1577e-113">資料結構的延伸會被指派大小可變大小的欄位，其中大小/位移是固定部分的一部分。</span><span class="sxs-lookup"><span data-stu-id="1577e-113">Extensions to data structures are assigned a variably sized field with size/offset being part of the fixed part.</span></span> <span data-ttu-id="1577e-114">TSPI 會針對每個資料結構描述允許的裝置特定延伸模組。</span><span class="sxs-lookup"><span data-stu-id="1577e-114">TSPI describes for each data structure what device-specific extensions are allowed.</span></span>

<span data-ttu-id="1577e-115">除了辨識特定的延伸模組識別碼之外，TAPI (可以代表應用程式運作) 必須協調應用程式和服務提供者運作的延伸模組版本號碼。</span><span class="sxs-lookup"><span data-stu-id="1577e-115">In addition to recognizing a specific extension identifier, TAPI (operating on behalf of an application) must negotiate the extension version number that the application and the service provider operate under.</span></span> <span data-ttu-id="1577e-116">這是使用 [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) 和 [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) 函數來完成。</span><span class="sxs-lookup"><span data-stu-id="1577e-116">This is done using the [**TSPI\_lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) and [**TSPI\_phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) functions.</span></span>

<span data-ttu-id="1577e-117">延伸模組識別碼是全域唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1577e-117">An extension identifier is a globally unique identifier.</span></span> <span data-ttu-id="1577e-118">延伸模組識別碼沒有中央登錄。</span><span class="sxs-lookup"><span data-stu-id="1577e-118">There is no central registry for extension identifiers.</span></span> <span data-ttu-id="1577e-119">相反地，它們是由工具組在本機由工具組提供的公用程式所產生。</span><span class="sxs-lookup"><span data-stu-id="1577e-119">Instead, they are generated locally by the manufacturer by a utility that is available with the toolkit.</span></span> <span data-ttu-id="1577e-120">此數位是由各部分組成，例如 (唯一) LAN 位址、一天中的時間和亂數字，以保證全域唯一性。</span><span class="sxs-lookup"><span data-stu-id="1577e-120">The number is made up of parts such as a (unique) LAN address, time of day, and random number, to guarantee global uniqueness.</span></span> <span data-ttu-id="1577e-121">全域唯一識別碼的設計目的是要與 HP/DEC 通用唯一識別碼區別，因此完全與其相容。</span><span class="sxs-lookup"><span data-stu-id="1577e-121">Globally unique identifiers are designed to be distinguishable from HP/DEC universally unique identifiers and are thus fully compatible with them.</span></span>

 

 
