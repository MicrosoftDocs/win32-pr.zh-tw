---
description: 訊息是用來通知應用程式非同步事件。 所有這些訊息都會透過應用程式在 lineInitializeEx 中指定的訊息通知機制傳送至應用程式。
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: TAPI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980588"
---
# <a name="tapi-messages"></a><span data-ttu-id="7284f-104">TAPI 訊息</span><span class="sxs-lookup"><span data-stu-id="7284f-104">TAPI Messages</span></span>

<span data-ttu-id="7284f-105">訊息是用來通知應用程式非同步事件。</span><span class="sxs-lookup"><span data-stu-id="7284f-105">Messages are used to notify the application of asynchronous events.</span></span> <span data-ttu-id="7284f-106">所有這些訊息都會透過應用程式在 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)中指定的訊息通知機制傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="7284f-106">All of these messages are sent to the application through the message notification mechanism that the application specified in [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="7284f-107">訊息一律包含相關物件的控制碼 (phone、line 或 call) ，應用程式可以使用此控制碼來判斷訊息類型。</span><span class="sxs-lookup"><span data-stu-id="7284f-107">The message always contains a handle to the relevant object (phone, line, or call), which the application can use to determine the message type.</span></span>

<span data-ttu-id="7284f-108">某些訊息是用來通知應用程式有關物件狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="7284f-108">Certain messages are used to notify the application about a change in an object's status.</span></span> <span data-ttu-id="7284f-109">這些訊息會提供物件控制碼，並指出已變更的狀態專案。</span><span class="sxs-lookup"><span data-stu-id="7284f-109">These messages provide the object handle and give an indication of which status item has changed.</span></span> <span data-ttu-id="7284f-110">應用程式可以呼叫物件的適當「取得狀態」功能，以取得物件的完整狀態。</span><span class="sxs-lookup"><span data-stu-id="7284f-110">The application can call the appropriate "get status" function of the object to obtain the object's full status.</span></span>

<span data-ttu-id="7284f-111">當事件發生時，可以將訊息傳送至零個、一個或多個應用程式。</span><span class="sxs-lookup"><span data-stu-id="7284f-111">When an event occurs, messages can be sent to zero, one, or more applications.</span></span> <span data-ttu-id="7284f-112">訊息的目標應用程式取決於許多不同的因素，包括訊息的意義、應用程式對物件的許可權、應用程式是否起始訊息為直接結果的要求，以及已由應用程式設定的訊息遮罩。</span><span class="sxs-lookup"><span data-stu-id="7284f-112">The target applications for a message are determined by a number of different factors including the meaning of the message, the application's privilege to the object, whether or not the application initiated the request for which the message is a direct result, and the message masking that has been set by the application.</span></span> <span data-ttu-id="7284f-113">請注意下列有關訊息的要點：</span><span class="sxs-lookup"><span data-stu-id="7284f-113">Note the following points about messages:</span></span>

-   <span data-ttu-id="7284f-114">非同步回復訊息只會傳送到發出要求的應用程式，而且無法遮罩。</span><span class="sxs-lookup"><span data-stu-id="7284f-114">Asynchronous reply messages are only sent to the application that originated the request and cannot be masked.</span></span>
-   <span data-ttu-id="7284f-115">發出數位或語氣產生或數位收集的訊息，只會傳送到要求數位或語氣產生的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7284f-115">Messages that signal the completion of digit or tone generation or the gathering of digits are only sent to the application that requested the digit or tone generation.</span></span>
-   <span data-ttu-id="7284f-116">指出行或位址狀態變更的訊息會傳送至已開啟該行的所有應用程式，只要訊息已透過 [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)啟用即可。</span><span class="sxs-lookup"><span data-stu-id="7284f-116">Messages that indicate line or address state changes are sent to all applications that have opened the line, so long as the message has been enabled through [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span>
-   <span data-ttu-id="7284f-117">指出撥號狀態和呼叫資訊變更的訊息會傳送至所有具有呼叫控制碼的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7284f-117">Messages that indicate call state and call information changes are sent to all applications that have a handle to the call.</span></span>
-   <span data-ttu-id="7284f-118">表示數位偵測、語氣偵測或媒體類型偵測的訊息會傳送給要求監視該事件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7284f-118">Messages that signal a digit detection, tone detection, or media type detection are sent to the applications that requested monitoring of that event.</span></span>

<span data-ttu-id="7284f-119">本節包含下列 TAPI 訊息的參考資訊：</span><span class="sxs-lookup"><span data-stu-id="7284f-119">This section contains the reference information for the following TAPI messages:</span></span>

-   [<span data-ttu-id="7284f-120">輔助電話語音訊息</span><span class="sxs-lookup"><span data-stu-id="7284f-120">Assisted Telephony Messages</span></span>](assisted-telephony-messages.md)
-   [<span data-ttu-id="7284f-121">撥打電話中心訊息</span><span class="sxs-lookup"><span data-stu-id="7284f-121">Call Center Messages</span></span>](call-center-messages.md)
-   [<span data-ttu-id="7284f-122">格式化的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="7284f-122">Formatted Error Messages</span></span>](formatted-error-messages.md)
-   [<span data-ttu-id="7284f-123">線路裝置訊息</span><span class="sxs-lookup"><span data-stu-id="7284f-123">Line Device Messages</span></span>](line-device-messages.md)
-   [<span data-ttu-id="7284f-124">手機裝置訊息</span><span class="sxs-lookup"><span data-stu-id="7284f-124">Phone Device Messages</span></span>](phone-device-messages.md)

 

 



