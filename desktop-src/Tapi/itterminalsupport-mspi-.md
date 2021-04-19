---
description: 如果有 MSP 存在，就會在位址物件上公開 ITTerminalSupport 介面。 此介面的方法可讓應用程式探索可用的終端機及/或建立一個，並取得所需終端機物件的指標。
ms.assetid: 39cb9734-3e70-4e37-9358-c638c6618c11
title: 'ITTerminalSupport (MSPI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63822f55742d5a4c7a0114abeb625f2393a51ae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978398"
---
# <a name="itterminalsupport-mspi"></a><span data-ttu-id="faf20-104">ITTerminalSupport (MSPI) </span><span class="sxs-lookup"><span data-stu-id="faf20-104">ITTerminalSupport (MSPI)</span></span>

<span data-ttu-id="faf20-105">如果有 MSP 存在，就會在 [位址物件](address-object.md)上公開 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)介面。</span><span class="sxs-lookup"><span data-stu-id="faf20-105">The [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is exposed on an [Address object](address-object.md) if an MSP exists.</span></span> <span data-ttu-id="faf20-106">此介面的方法可讓應用程式探索可用的終端機及/或建立一個，並取得所需 [終端機物件](terminal-object.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="faf20-106">The methods of this interface allow an application to discover available terminals and/or create one, and get pointers to required [Terminal objects](terminal-object.md).</span></span>

<span data-ttu-id="faf20-107">[**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)介面是由 MSP 所執行，而且如果沒有與該位址相關聯的媒體服務提供者，就無法使用。</span><span class="sxs-lookup"><span data-stu-id="faf20-107">The [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is implemented by an MSP and is not available if there is no media service provider associated with the address.</span></span> <span data-ttu-id="faf20-108">如需此介面的詳細資訊，請參閱 MSP 介面一節中的 **ITTerminalSupport** 。</span><span class="sxs-lookup"><span data-stu-id="faf20-108">Please see **ITTerminalSupport** in the MSP Interface section for details on this interface.</span></span>

 

 
