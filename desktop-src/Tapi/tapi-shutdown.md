---
description: 需要適當地關閉通訊會話和整個應用程式，才能防止資源在不再需要它們的呼叫或應用程式中保持聯繫。
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: TAPI 關機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990428"
---
# <a name="tapi-shutdown"></a><span data-ttu-id="56065-103">TAPI 關機</span><span class="sxs-lookup"><span data-stu-id="56065-103">TAPI Shutdown</span></span>

<span data-ttu-id="56065-104">需要適當地關閉通訊會話和整個應用程式，才能防止資源在不再需要它們的呼叫或應用程式中保持聯繫。</span><span class="sxs-lookup"><span data-stu-id="56065-104">Proper shutdown of communications sessions and of an entire application is required to prevent resources from remaining tied up in calls or applications that no longer need them.</span></span>

<span data-ttu-id="56065-105">TAPI 提供一系列的功能和方法來協助處理。</span><span class="sxs-lookup"><span data-stu-id="56065-105">TAPI provides a series of functions and methods to assist in the process.</span></span> <span data-ttu-id="56065-106">很明顯地，應用程式也必須負責適當釋出配置的記憶體，不論是以資料結構或 COM 參考形式。</span><span class="sxs-lookup"><span data-stu-id="56065-106">Obviously, the application must also take responsibility for properly releasing allocated memory, whether in the form of data structures or COM references.</span></span>



| <span data-ttu-id="56065-107">TAPI 2.x 函數</span><span class="sxs-lookup"><span data-stu-id="56065-107">TAPI 2.x functions</span></span>                                                            | <span data-ttu-id="56065-108">Description</span><span class="sxs-lookup"><span data-stu-id="56065-108">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="56065-109">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="56065-109">**lineRegisterRequestRecipient**</span></span>](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="56065-110">將應用程式取消註冊為輔助電話語音通話的處理常式。</span><span class="sxs-lookup"><span data-stu-id="56065-110">Unregisters the application as a handler for assisted telephony calls.</span></span> |
| [<span data-ttu-id="56065-111">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="56065-111">**lineClose**</span></span>](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | <span data-ttu-id="56065-112">將應用程式與指定行呼叫的管理員中斷連接。</span><span class="sxs-lookup"><span data-stu-id="56065-112">Disconnects the application as a manager for calls on the given line.</span></span>  |
| [<span data-ttu-id="56065-113">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="56065-113">**lineShutdown**</span></span>](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | <span data-ttu-id="56065-114">關閉應用程式行抽象的使用方式。</span><span class="sxs-lookup"><span data-stu-id="56065-114">Shuts down the application's usage of the line abstraction.</span></span>            |



 



| <span data-ttu-id="56065-115">TAPI 3.x 介面或方法</span><span class="sxs-lookup"><span data-stu-id="56065-115">TAPI 3.x interfaces or methods</span></span>                                            | <span data-ttu-id="56065-116">Description</span><span class="sxs-lookup"><span data-stu-id="56065-116">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="56065-117">**ITTAPI::UnregisterNotifications**</span><span class="sxs-lookup"><span data-stu-id="56065-117">**ITTAPI::UnregisterNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | <span data-ttu-id="56065-118">移除應用程式所執行的任何事件通知註冊。</span><span class="sxs-lookup"><span data-stu-id="56065-118">Removes any event notification registrations performed by the application.</span></span> |
| [<span data-ttu-id="56065-119">**ITTAPI：： Shutdown**</span><span class="sxs-lookup"><span data-stu-id="56065-119">**ITTAPI::Shutdown**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | <span data-ttu-id="56065-120">中斷應用程式與呼叫管理員的連接。</span><span class="sxs-lookup"><span data-stu-id="56065-120">Disconnects the application as a call manager.</span></span>                             |



 

 

 
