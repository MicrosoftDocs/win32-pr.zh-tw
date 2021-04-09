---
description: 感應器管理員物件可存取可供您使用的感應器。
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: 感應器管理員物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112624"
---
# <a name="the-sensor-manager-object"></a><span data-ttu-id="c272c-103">感應器管理員物件</span><span class="sxs-lookup"><span data-stu-id="c272c-103">The Sensor Manager Object</span></span>

<span data-ttu-id="c272c-104">感應器管理員物件可存取可供您使用的感應器。</span><span class="sxs-lookup"><span data-stu-id="c272c-104">The sensor manager object provides access to the sensors that are available for your use.</span></span>

<span data-ttu-id="c272c-105">若要使用感應器 API，您必須先呼叫 COM **CoCreateInstance** 方法來建立感應器管理員物件的實例，並取得其介面（名為 [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)）的指標。</span><span class="sxs-lookup"><span data-stu-id="c272c-105">To use the Sensor API, you must first call the COM **CoCreateInstance** method to create an instance of the sensor manager object and retrieve a pointer to its interface, named [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span></span> <span data-ttu-id="c272c-106">感應器管理員會維護可用感應器的清單。</span><span class="sxs-lookup"><span data-stu-id="c272c-106">The sensor manager maintains the list of available sensors.</span></span> <span data-ttu-id="c272c-107">您可以使用 **ISensorManager** 來呼叫依類別或類型抓取感應器群組的方法，或者您也可以使用其唯一識別碼來呼叫方法，以取得特定感應器。</span><span class="sxs-lookup"><span data-stu-id="c272c-107">You can use **ISensorManager** to call methods that retrieve groups of sensors by category or by type, or you can call a method to retrieve a particular sensor by using its unique ID.</span></span> <span data-ttu-id="c272c-108">感應器管理員也可讓您註冊來接收事件，以在新感應器連線到平臺時通知您。</span><span class="sxs-lookup"><span data-stu-id="c272c-108">The sensor manager also enables you to register to receive an event that notifies you when a new sensor has been connected to the platform.</span></span>

<span data-ttu-id="c272c-109">感應器管理員有時會提供感應器的指標，但使用者尚未啟用感應器。</span><span class="sxs-lookup"><span data-stu-id="c272c-109">Sometimes, the sensor manager provides a pointer to a sensor, but the user has not enabled the sensor.</span></span> <span data-ttu-id="c272c-110">例如，您通常可以在使用者啟用感應器之前，先取出非私用感應器屬性的值，例如感應器製造商或型號。</span><span class="sxs-lookup"><span data-stu-id="c272c-110">For example, you can often retrieve values for non-private sensor properties, such as the sensor manufacturer or model, before the user enables the sensor.</span></span> <span data-ttu-id="c272c-111">此資訊可協助您決定是否要要求使用者提供使用感應器的許可權。</span><span class="sxs-lookup"><span data-stu-id="c272c-111">This information can help you to decide whether to ask the user for permission to use the sensor.</span></span> <span data-ttu-id="c272c-112">您可以呼叫 [**ISensorManager：： RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) ，以提示使用者啟用特定感應器或感應器集合。</span><span class="sxs-lookup"><span data-stu-id="c272c-112">You can call [**ISensorManager::RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) to prompt the user to enable a particular sensor or collection of sensors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c272c-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="c272c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c272c-114">管理使用者權限</span><span class="sxs-lookup"><span data-stu-id="c272c-114">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> <dt>

[<span data-ttu-id="c272c-115">要求使用者權限</span><span class="sxs-lookup"><span data-stu-id="c272c-115">Requesting User Permissions</span></span>](requesting-user-permissions.md)
</dt> </dl>

 

 
