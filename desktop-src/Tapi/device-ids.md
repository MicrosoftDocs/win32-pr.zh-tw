---
description: 其他 TAPI 電話功能會使用開放電話裝置的控制碼來識別開啟的電話裝置。
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: 裝置識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970815"
---
# <a name="device-ids"></a><span data-ttu-id="5ade0-103">裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="5ade0-103">Device IDs</span></span>

<span data-ttu-id="5ade0-104">其他 TAPI 電話功能會使用開放電話裝置的控制碼來識別開啟的電話裝置。</span><span class="sxs-lookup"><span data-stu-id="5ade0-104">Other TAPI phone functions use a handle to an open phone device to identify the open phone device.</span></span> <span data-ttu-id="5ade0-105">使用電話裝置識別碼參數的電話裝置的唯一功能 (與電話控制碼) 的不同，是 [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) 和 [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) 函式。</span><span class="sxs-lookup"><span data-stu-id="5ade0-105">The only functions for phone devices that take a phone device identifier parameter (as opposed to a phone handle) are the [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) functions.</span></span> <span data-ttu-id="5ade0-106">應用程式可以使用 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) 函式搭配電話控制碼作為參數，來取得電話的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ade0-106">An application can retrieve the phone's device identifier by using the [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function with the phone handle as a parameter.</span></span>

<span data-ttu-id="5ade0-107">應用程式也可以藉由叫用 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)，取得與已開啟電話相關聯之各種裝置類別的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ade0-107">An application can also obtain device identifiers for various device classes associated with an opened phone by invoking [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span> <span data-ttu-id="5ade0-108">請參閱裝置類別名稱的 [TAPI 裝置類別](tapi-device-classes.md) 。</span><span class="sxs-lookup"><span data-stu-id="5ade0-108">See [TAPI Device Classes](tapi-device-classes.md) for device class names.</span></span>

<span data-ttu-id="5ade0-109">此函式會採用電話控制碼和裝置類別描述。</span><span class="sxs-lookup"><span data-stu-id="5ade0-109">This function takes a phone handle and a device class description.</span></span> <span data-ttu-id="5ade0-110">它會傳回與開啟的電話裝置相關聯之指定裝置類別之裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ade0-110">It returns the device identifier for the device of the given device class that is associated with the open phone device.</span></span> <span data-ttu-id="5ade0-111">如果裝置類別是「tapi/電話」，則會傳回電話裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ade0-111">If the device class is "tapi/phone", the device identifier of the phone device is returned.</span></span>

<span data-ttu-id="5ade0-112">相較于行裝置（基本線路服務會提供對等的 POTS），不會為電話裝置定義最低保證的函式集合。</span><span class="sxs-lookup"><span data-stu-id="5ade0-112">In contrast with line devices, for which the basic line services provide the equivalent of POTS, no minimum guaranteed set of functions is defined for phone devices.</span></span> <span data-ttu-id="5ade0-113">雖然每個電話裝置至少都提供本節所述的函式和訊息，但它們並不提供實體電話裝置上的任何實際操作。</span><span class="sxs-lookup"><span data-stu-id="5ade0-113">While each phone device provides at least the functions and messages described in this section, they do not offer any actual operations on the physical phone device.</span></span>

 

 



