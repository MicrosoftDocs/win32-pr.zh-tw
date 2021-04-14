---
title: Windows 事件收集器列舉
description: 下表列出 Windows 事件收集器 SDK 的列舉。
ms.assetid: 3775aa7c-ef35-4534-b709-15624fd7a90d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d2617c6eb0052ec1ac41d5f197d9216c253054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372280"
---
# <a name="windows-event-collector-enumerations"></a><span data-ttu-id="d2a22-103">Windows 事件收集器列舉</span><span class="sxs-lookup"><span data-stu-id="d2a22-103">Windows Event Collector Enumerations</span></span>

<span data-ttu-id="d2a22-104">下表列出 Windows 事件收集器 SDK 的列舉。</span><span class="sxs-lookup"><span data-stu-id="d2a22-104">The following table lists the enumerations of the Windows Event Collector SDK.</span></span>



| <span data-ttu-id="d2a22-105">列舉型別</span><span class="sxs-lookup"><span data-stu-id="d2a22-105">Enumeration</span></span>                                                                                               | <span data-ttu-id="d2a22-106">描述</span><span class="sxs-lookup"><span data-stu-id="d2a22-106">Description</span></span>                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2a22-107">**EC 訂用帳戶設定 \_ \_ \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="d2a22-107">**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode)                       | <span data-ttu-id="d2a22-108">指定變更訂用帳戶預設值的不同設定模式。</span><span class="sxs-lookup"><span data-stu-id="d2a22-108">Specifies different configuration modes that change the default settings for a subscription.</span></span>                                            |
| [<span data-ttu-id="d2a22-109">**EC \_ 訂用帳戶 \_ 內容 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="d2a22-109">**EC\_SUBSCRIPTION\_CONTENT\_FORMAT**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_content_format)                               | <span data-ttu-id="d2a22-110">指定在事件傳送到事件收集器電腦之前，要如何在傳送事件的電腦上呈現事件。</span><span class="sxs-lookup"><span data-stu-id="d2a22-110">Specifies how events will be rendered on the computer that sends the events before the events are sent to the event collector computer.</span></span> |
| [<span data-ttu-id="d2a22-111">**EC \_ 訂用帳戶 \_ 認證 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d2a22-111">**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type)                           | <span data-ttu-id="d2a22-112">指定與事件來源通訊時所要使用的認證類型。</span><span class="sxs-lookup"><span data-stu-id="d2a22-112">Specifies the type of credentials to use when communicating with event sources.</span></span>                                                         |
| [<span data-ttu-id="d2a22-113">**EC \_ 訂閱 \_ 傳遞 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="d2a22-113">**EC\_SUBSCRIPTION\_DELIVERY\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_delivery_mode)                                 | <span data-ttu-id="d2a22-114">指定如何透過事件訂閱傳遞事件， (使用推播或提取模型) 。</span><span class="sxs-lookup"><span data-stu-id="d2a22-114">Specifies how events are delivered through an event subscription (using a push or pull model).</span></span>                                          |
| [<span data-ttu-id="d2a22-115">**EC \_ 訂用帳戶 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="d2a22-115">**EC\_SUBSCRIPTION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)                                     | <span data-ttu-id="d2a22-116">定義值，以識別用於訂用帳戶設定的事件訂閱屬性。</span><span class="sxs-lookup"><span data-stu-id="d2a22-116">Defines values to identify event subscription properties used for subscription configuration.</span></span>                                           |
| [<span data-ttu-id="d2a22-117">**EC 訂用帳戶執行時間狀態作用中 \_ \_ \_ \_ \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="d2a22-117">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_ACTIVE\_STATUS**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_active_status) | <span data-ttu-id="d2a22-118">指定訂用帳戶的狀態或與訂用帳戶相關的事件來源。</span><span class="sxs-lookup"><span data-stu-id="d2a22-118">Specifies the status of a subscription or an event source with respect to a subscription.</span></span>                                               |
| [<span data-ttu-id="d2a22-119">**EC \_ 訂用帳戶 \_ 執行時間 \_ 狀態 \_ 資訊 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="d2a22-119">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_INFO\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_info_id)             | <span data-ttu-id="d2a22-120">指定值，這個值會識別事件來源或訂閱之執行時間狀態的屬性。</span><span class="sxs-lookup"><span data-stu-id="d2a22-120">Specifies a value that identifies a property of the runtime status of an event source or a subscription.</span></span>                                |
| [<span data-ttu-id="d2a22-121">**EC \_ 訂用帳戶 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d2a22-121">**EC\_SUBSCRIPTION\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_type)                                                    | <span data-ttu-id="d2a22-122">指定要在來源起始或收集器起始的訂閱)  (使用的訂用帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="d2a22-122">Specifies the type of subscription to use (a source initiated or collector initiated subscription).</span></span>                                     |
| [<span data-ttu-id="d2a22-123">**EC \_ 變異 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d2a22-123">**EC\_VARIANT\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_variant_type)                                                              | <span data-ttu-id="d2a22-124">定義值，這些值會指定 Windows 事件收集器函式中使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="d2a22-124">Defines the values that specify the data types that are used in the Windows Event Collector functions.</span></span>                                  |



 

 

 




