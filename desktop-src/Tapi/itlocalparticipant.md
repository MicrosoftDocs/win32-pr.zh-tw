---
description: 當 IPConf MSP 支援呼叫時，會在資料流程物件上公開 ITLocalParticipant 介面。
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: 'ITLocalParticipant 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980120"
---
# <a name="itlocalparticipant-interface"></a><span data-ttu-id="c67b4-103">ITLocalParticipant 介面</span><span class="sxs-lookup"><span data-stu-id="c67b4-103">ITLocalParticipant interface</span></span>

<span data-ttu-id="c67b4-104">當 IPConf MSP 支援呼叫時，會在資料流程物件上公開 **ITLocalParticipant** 介面。</span><span class="sxs-lookup"><span data-stu-id="c67b4-104">The **ITLocalParticipant** interface is exposed on the stream object when the IPConf MSP supports the call.</span></span> <span data-ttu-id="c67b4-105">MSP 會實行可讓應用程式取得和設定參與者資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="c67b4-105">The MSP implements methods that allow an application to get and set participant information.</span></span> <span data-ttu-id="c67b4-106">**ITLocalParticipant** 介面是藉由在 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)上呼叫 **QueryInterface** 來建立。</span><span class="sxs-lookup"><span data-stu-id="c67b4-106">The **ITLocalParticipant** interface is created by calling **QueryInterface** on [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>

## <a name="members"></a><span data-ttu-id="c67b4-107">成員</span><span class="sxs-lookup"><span data-stu-id="c67b4-107">Members</span></span>

<span data-ttu-id="c67b4-108">**ITLocalParticipant** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c67b4-108">The **ITLocalParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c67b4-109">**ITLocalParticipant** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c67b4-109">**ITLocalParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="c67b4-110">方法</span><span class="sxs-lookup"><span data-stu-id="c67b4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c67b4-111">方法</span><span class="sxs-lookup"><span data-stu-id="c67b4-111">Methods</span></span>

<span data-ttu-id="c67b4-112">**ITLocalParticipant** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c67b4-112">The **ITLocalParticipant** interface has these methods.</span></span>



| <span data-ttu-id="c67b4-113">方法</span><span class="sxs-lookup"><span data-stu-id="c67b4-113">Method</span></span>                                                                                     | <span data-ttu-id="c67b4-114">描述</span><span class="sxs-lookup"><span data-stu-id="c67b4-114">Description</span></span>                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="c67b4-115">**取得 \_ LocalParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="c67b4-115">**get\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-get-localparticipanttypedinfo.md) | <span data-ttu-id="c67b4-116">取得參與者資訊，例如電子郵件名稱或地理位置。</span><span class="sxs-lookup"><span data-stu-id="c67b4-116">Gets participant information, such as e-mail name or geographical location.</span></span><br/> |
| [<span data-ttu-id="c67b4-117">**put \_ LocalParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="c67b4-117">**put\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-put-localparticipanttypedinfo.md) | <span data-ttu-id="c67b4-118">設定參與者資訊。</span><span class="sxs-lookup"><span data-stu-id="c67b4-118">Sets participant information.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="c67b4-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c67b4-119">Requirements</span></span>



| <span data-ttu-id="c67b4-120">需求</span><span class="sxs-lookup"><span data-stu-id="c67b4-120">Requirement</span></span> | <span data-ttu-id="c67b4-121">值</span><span class="sxs-lookup"><span data-stu-id="c67b4-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c67b4-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="c67b4-122">TAPI version</span></span><br/> | <span data-ttu-id="c67b4-123">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c67b4-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c67b4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c67b4-124">Header</span></span><br/>       | <dl> <span data-ttu-id="c67b4-125"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="c67b4-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="c67b4-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="c67b4-126">Library</span></span><br/>      | <dl> <span data-ttu-id="c67b4-127"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="c67b4-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c67b4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c67b4-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="c67b4-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c67b4-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c67b4-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c67b4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67b4-131">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="c67b4-131">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

