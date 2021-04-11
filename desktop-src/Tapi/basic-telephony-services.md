---
description: 基本電話語音服務是電話語音規格的最小子集。
ms.assetid: 997e405f-41fa-4aeb-8700-3f9f61430c88
title: 基本電話語音服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6623c7481472daa074f5d8bc627e4a873ec0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114932"
---
# <a name="basic-telephony-services"></a><span data-ttu-id="75016-103">基本電話語音服務</span><span class="sxs-lookup"><span data-stu-id="75016-103">Basic Telephony Services</span></span>

<span data-ttu-id="75016-104">基本電話語音服務是電話語音規格的最小子集。</span><span class="sxs-lookup"><span data-stu-id="75016-104">Basic Telephony services are a minimal subset of the Telephony specification.</span></span> <span data-ttu-id="75016-105">因為所有服務提供者都必須支援基本電話語音服務的功能，所以使用這些功能的應用程式將可與任何 TAPI 服務提供者搭配使用。</span><span class="sxs-lookup"><span data-stu-id="75016-105">Because all service providers must support the functions of Basic Telephony services, applications that use only these functions will work with any TAPI service provider.</span></span> <span data-ttu-id="75016-106">基本電話語音中包含的功能，大致上與 POTS 的功能相對應。</span><span class="sxs-lookup"><span data-stu-id="75016-106">The functionality contained in Basic Telephony roughly corresponds to the features of POTS.</span></span>

<span data-ttu-id="75016-107">許多程式設計人員只會使用基本電話語音所提供的服務。</span><span class="sxs-lookup"><span data-stu-id="75016-107">Many programmers will use only the services that Basic Telephony provides.</span></span> <span data-ttu-id="75016-108">有些人（例如針對 PBX 電話系統撰寫程式碼的程式碼）將需要補充電話語音的功能。</span><span class="sxs-lookup"><span data-stu-id="75016-108">Others, such as those writing code for PBX phone systems, will need the functions of Supplementary Telephony.</span></span>

<span data-ttu-id="75016-109">如需基本電話語音功能的清單，請參閱 [TAPI 快速功能參考](./tapi-quick-function-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="75016-109">For a list of the functions of Basic Telephony, see [TAPI Quick Function Reference](./tapi-quick-function-reference.md).</span></span>

<span data-ttu-id="75016-110">因為不會假設所有服務提供者都提供手機裝置控制，所以會將電話裝置服務視為選擇性。</span><span class="sxs-lookup"><span data-stu-id="75016-110">Because control of phone devices is not assumed to be offered by all service providers, phone-device services are considered to be optional.</span></span> <span data-ttu-id="75016-111">也就是說，它們不是基本電話語音的一部分。</span><span class="sxs-lookup"><span data-stu-id="75016-111">That is, they are not a part of Basic Telephony.</span></span> <span data-ttu-id="75016-112">如需電話裝置服務的清單，請參閱 [補充電話語音服務](supplementary-telephony-services.md);如需電話裝置的詳細資訊，請參閱 [TAPI 裝置類別](./tapi-device-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="75016-112">For a list of phone-device services, see [Supplementary Telephony Services](supplementary-telephony-services.md); for more information on phone devices, see [TAPI Device Classes](./tapi-device-classes.md).</span></span>

 

 
