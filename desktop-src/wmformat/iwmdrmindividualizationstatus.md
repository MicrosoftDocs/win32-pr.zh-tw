---
title: IWMDRMIndividualizationStatus 介面
description: IWMDRMIndividualizationStatus 介面可讓您抓取有關個人化進度的 advanced status 資訊。此介面會與 MEWMDRMIndividualizationProgress 事件一起傳遞。
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- IWMDRMIndividualizationStatus 介面 windows 媒體格式
- IWMDRMIndividualizationStatus 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933489"
---
# <a name="iwmdrmindividualizationstatus-interface"></a><span data-ttu-id="8c7b6-105">IWMDRMIndividualizationStatus 介面</span><span class="sxs-lookup"><span data-stu-id="8c7b6-105">IWMDRMIndividualizationStatus interface</span></span>

<span data-ttu-id="8c7b6-106">**IWMDRMIndividualizationStatus** 介面可讓您抓取有關個人化進度的 advanced status 資訊。</span><span class="sxs-lookup"><span data-stu-id="8c7b6-106">The **IWMDRMIndividualizationStatus** interface enables retrieval of advanced status information about the progress of individualization.</span></span>

<span data-ttu-id="8c7b6-107">此介面會與 MEWMDRMIndividualizationProgress 事件一起傳遞。</span><span class="sxs-lookup"><span data-stu-id="8c7b6-107">This interface is delivered with MEWMDRMIndividualizationProgress events.</span></span> <span data-ttu-id="8c7b6-108">在 IWMDRMSecurity 的呼叫之間會產生許多這類事件 [**：:P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) 和自動完成的個人化程式（由產生 **MEWMDRMIndividualizationCompleted** 事件發出信號）。</span><span class="sxs-lookup"><span data-stu-id="8c7b6-108">Many such events are generated between a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) and the completion of the individualization process, which is signaled by the generation of an **MEWMDRMIndividualizationCompleted** event.</span></span>

<span data-ttu-id="8c7b6-109">若要取出 **IWMDRMIndividualizationStatus** 介面實例的指標，您必須先呼叫進度事件的 **IMFMediaEvent：： GetValue** 方法。</span><span class="sxs-lookup"><span data-stu-id="8c7b6-109">To retrieve a pointer to an instance of the **IWMDRMIndividualizationStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="8c7b6-110">您從事件中取出的值是實 **IWMDRMIndividualizationStatus** 介面之物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="8c7b6-110">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMIndividualizationStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="8c7b6-111">成員</span><span class="sxs-lookup"><span data-stu-id="8c7b6-111">Members</span></span>

<span data-ttu-id="8c7b6-112">**IWMDRMIndividualizationStatus** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="8c7b6-112">The **IWMDRMIndividualizationStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8c7b6-113">**IWMDRMIndividualizationStatus** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8c7b6-113">**IWMDRMIndividualizationStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="8c7b6-114">方法</span><span class="sxs-lookup"><span data-stu-id="8c7b6-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8c7b6-115">方法</span><span class="sxs-lookup"><span data-stu-id="8c7b6-115">Methods</span></span>

<span data-ttu-id="8c7b6-116">**IWMDRMIndividualizationStatus** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8c7b6-116">The **IWMDRMIndividualizationStatus** interface has these methods.</span></span>



| <span data-ttu-id="8c7b6-117">方法</span><span class="sxs-lookup"><span data-stu-id="8c7b6-117">Method</span></span>                                                       | <span data-ttu-id="8c7b6-118">描述</span><span class="sxs-lookup"><span data-stu-id="8c7b6-118">Description</span></span>                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="8c7b6-119">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="8c7b6-119">**GetStatus**</span></span>](iwmdrmindividualizationstatus-getstatus.md) | <span data-ttu-id="8c7b6-120">抓取有關個人化的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8c7b6-120">Retrieves detailed information about individualization.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8c7b6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c7b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c7b6-122">**介面**</span><span class="sxs-lookup"><span data-stu-id="8c7b6-122">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

