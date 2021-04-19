---
description: API 包含一種機制，可讓服務提供者廠商使用裝置特定的擴充功能來擴充電話語音 API。
ms.assetid: 02749ce5-40db-487e-b51e-e3692266342c
title: 擴充的電話語音服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a319f59f51643fb5bf13ec95800d40ffa6d8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989947"
---
# <a name="extended-telephony-services"></a><span data-ttu-id="4d2d7-103">擴充的電話語音服務</span><span class="sxs-lookup"><span data-stu-id="4d2d7-103">Extended Telephony Services</span></span>

<span data-ttu-id="4d2d7-104">API 包含一種機制，可讓服務提供者廠商使用裝置特定的擴充功能來擴充電話語音 API。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-104">The API contains a mechanism that allows service-provider vendors to extend the Telephony API using device-specific extensions.</span></span> <span data-ttu-id="4d2d7-105">擴充的電話語音服務 (或裝置特定的服務) 包含特定服務提供者所定義之 API 的所有延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-105">Extended Telephony services (or device-specific services) include all extensions to the API defined by a particular service provider.</span></span> <span data-ttu-id="4d2d7-106">因為 API 只會定義擴充機制，所以服務提供者必須完全指定 Extended-Telephony 服務行為的定義。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-106">Because the API defines only the extension mechanism, the service provider must completely specify the definition of the Extended-Telephony service behavior.</span></span>

## <a name="tapi-2x-extended-telephony"></a><span data-ttu-id="4d2d7-107">TAPI 2.x 擴充電話語音</span><span class="sxs-lookup"><span data-stu-id="4d2d7-107">TAPI 2.x Extended Telephony</span></span>

<span data-ttu-id="4d2d7-108">擴充機制可讓服務提供者廠商為某些列舉型別和位旗標定義新的值，並將成員新增至大部分的資料結構。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-108">The extension mechanism allows service-provider vendors to define new values for some enumeration types and bit flags and to add members to most data structures.</span></span> <span data-ttu-id="4d2d7-109">擴充功能的解讀會以服務提供者的延伸模組識別碼為依據，這是一組支援的延伸模組規格的識別碼，可跨數個製造商。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-109">The interpretation of extensions is keyed off the service provider's extension identifier, an identifier for the specification of the set of extensions supported, which may cross several manufacturers.</span></span> <span data-ttu-id="4d2d7-110">API 中會提供特殊的函式和訊息（例如 [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) 和 [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) ），以允許應用程式直接與服務提供者通訊。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-110">Special functions and messages such as [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) and [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) are provided in the API to allow an application to directly communicate with a service provider.</span></span> <span data-ttu-id="4d2d7-111">服務提供者也會定義每個函數的參數。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-111">The service provider also defines the parameters for each function.</span></span>

<span data-ttu-id="4d2d7-112">廠商不需要註冊即可指派延伸模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-112">Vendors are not required to register in order to be assigned extension identifiers.</span></span> <span data-ttu-id="4d2d7-113">相反地，會在平臺軟體發展工具組中提供稱為 EXTIDGEN (Extidgen.exe) 的公用程式， (SDK) 允許本機產生延伸模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-113">Instead, a utility called EXTIDGEN (Extidgen.exe) is provided within the Platform Software Development Kit (SDK) that allows the local generation of extension identifiers.</span></span> <span data-ttu-id="4d2d7-114">這個唯一的識別碼是由乙太網路介面卡位址、亂數字和一天中的時間所組成。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-114">This unique identifier is composed of an Ethernet-adapter address, a random number, and the time of day.</span></span> <span data-ttu-id="4d2d7-115">在散發) 之前，會將識別碼指派給一組延伸 (，而不是指派給這些擴充功能的每個個別實例。</span><span class="sxs-lookup"><span data-stu-id="4d2d7-115">An identifier is assigned to a set of extensions (before distribution), not to each individual instance of an implementation of those extensions.</span></span>

 

 
