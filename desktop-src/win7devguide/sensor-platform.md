---
title: 感應器平臺
description: Windows 7 已改變開發人員使用感應器的方式。
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023713"
---
# <a name="sensor-platform"></a><span data-ttu-id="899fb-103">感應器平臺</span><span class="sxs-lookup"><span data-stu-id="899fb-103">Sensor Platform</span></span>

<span data-ttu-id="899fb-104">Windows 7 已改變開發人員使用感應器的方式。</span><span class="sxs-lookup"><span data-stu-id="899fb-104">Windows 7 has changed how developers use sensors.</span></span> <span data-ttu-id="899fb-105">它包含對感應器的原生支援，並透過新的開發平臺（用於處理感應器）擴充，包括定位感應器，例如 (GPS) 裝置的全球定位系統。</span><span class="sxs-lookup"><span data-stu-id="899fb-105">It includes native support for sensors, expanded by a new development platform for working with sensors, including location sensors, such as Global Positioning Systems (GPS) devices.</span></span>

<span data-ttu-id="899fb-106">*Windows 定位* api 是以感應器平臺為基礎，這是新的 windows 7 功能，可讓應用程式開發人員存取使用者的實體位置資訊。</span><span class="sxs-lookup"><span data-stu-id="899fb-106">Built on the Sensor Platform, the *Windows Location* APIs are a new Windows 7 feature that enables application developers to access the user's physical location information.</span></span> <span data-ttu-id="899fb-107">*Windows 定位* api 可以抽象化硬體、同時支援多個應用程式，並在不同的技術之間無縫切換，讓應用程式開發人員不必承擔管理這些限制的負擔。</span><span class="sxs-lookup"><span data-stu-id="899fb-107">The *Windows Location* APIs can abstract hardware, simultaneously support multiple applications, and seamlessly switch between different technologies, relieving the application developer of the burden of managing these constraints.</span></span> <span data-ttu-id="899fb-108">使用 c + + 程式設計語言 (程式設計人員可以使用 *位置* api，方法是熟悉元件物件模型 (COM) ) ，或使用指令碼語言（例如 Microsoft JScript）中的 com 物件。</span><span class="sxs-lookup"><span data-stu-id="899fb-108">The *Location* APIs can be used by programmers through the C++ programming language (by programmers familiar with Component Object Model (COM)), or by using COM objects in scripting languages, such as Microsoft JScript.</span></span> <span data-ttu-id="899fb-109">腳本支援可讓您輕鬆存取專案的位置資料，例如小工具。</span><span class="sxs-lookup"><span data-stu-id="899fb-109">Scripting support gives easy access to location data for projects such as gadgets.</span></span>

<span data-ttu-id="899fb-110">Windows 7 提供一個穩固且便於使用的平臺，可讓您使用感應器裝置，例如環境光線感應器或溫度測計，在 Windows 應用程式中建立環境感知。</span><span class="sxs-lookup"><span data-stu-id="899fb-110">Windows 7 provides a solid, easy-to-use platform for using sensor devices, such as an ambient light sensor or a temperature gauge, to create environmental awareness in Windows applications.</span></span> <span data-ttu-id="899fb-111">電腦可以使用內建于電腦、透過有線或無線連線連線，或是透過網路或 *網際網路* 連線的感應器。</span><span class="sxs-lookup"><span data-stu-id="899fb-111">PCs can use sensors that are built into the computer, connected through wired or wireless connections, or connected through a network or the *Internet*.</span></span>

<span data-ttu-id="899fb-112">*感應器* 和 *位置* api 提供了一種標準方式來探索感應器，並以程式設計方式存取感應器提供的資料。</span><span class="sxs-lookup"><span data-stu-id="899fb-112">The *Sensor* and *Location* APIs provide a standard way to discover sensors, and to programmatically access data that sensors provide.</span></span>

<span data-ttu-id="899fb-113">*感應器* 控制台可讓使用者啟用或停用感應器、控制可能公開敏感性資料之感應器的存取、查看感應器屬性，以及變更感應器的描述。</span><span class="sxs-lookup"><span data-stu-id="899fb-113">The *Sensor* control panel lets users enable or disable sensors, control access to sensors that might expose sensitive data, view sensor properties, and change the descriptions of sensors.</span></span>

<span data-ttu-id="899fb-114">[感應器類別延伸](/windows-hardware/drivers/sensors/about-the-sensor-class-extension)是感應器平臺驅動程式開發模型的核心部分。</span><span class="sxs-lookup"><span data-stu-id="899fb-114">The [Sensor Class Extension](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) is a core part of the driver development model for the Sensor Platform.</span></span> <span data-ttu-id="899fb-115">它提供下列機制，在撰寫 [使用者模式驅動程式架構 () ](https://developer.microsoft.com/windows/hardware) 感應器驅動程式時，會使用這些機制：</span><span class="sxs-lookup"><span data-stu-id="899fb-115">It provides the following mechanisms, which are used when writing a [User-Mode Driver Framework (UMDF)](https://developer.microsoft.com/windows/hardware) sensor driver:</span></span>

-   <span data-ttu-id="899fb-116">與感應器平臺整合</span><span class="sxs-lookup"><span data-stu-id="899fb-116">Integration with the Sensor Platform</span></span>
-   <span data-ttu-id="899fb-117">安全性強制</span><span class="sxs-lookup"><span data-stu-id="899fb-117">Security enforcement</span></span>

## <a name="related-topics"></a><span data-ttu-id="899fb-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="899fb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="899fb-119">感應器 API</span><span class="sxs-lookup"><span data-stu-id="899fb-119">Sensor API</span></span>](../sensorsapi/portal.md)
</dt> <dt>