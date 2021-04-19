---
description: ITAttributeList 介面會提供方法來取得和設定未中斷的屬性。
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: 'ITAttributeList 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994871"
---
# <a name="itattributelist-interface"></a><span data-ttu-id="cf0d9-103">ITAttributeList 介面</span><span class="sxs-lookup"><span data-stu-id="cf0d9-103">ITAttributeList interface</span></span>

<span data-ttu-id="cf0d9-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cf0d9-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="cf0d9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cf0d9-106">**ITAttributeList** 介面會提供方法來取得和設定未中斷的屬性。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-106">The **ITAttributeList** interface supplies methods for getting and setting of uninterpreted attributes.</span></span> <span data-ttu-id="cf0d9-107">關於會話描述項通訊協定中的屬性字串位置 (SDP，請參閱 RFC 2327) 封包，方法會假設所有屬性字串都存在於指定媒體屬性之前，以及在所有通用屬性之後。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-107">Regarding the position of the attribute strings in a Session Descriptor Protocol (SDP, see RFC 2327) packet, the methods assume that all attribute strings exist just before the media attributes are specified and after all the common attributes.</span></span> <span data-ttu-id="cf0d9-108">**ITAttributeList** 介面是藉由在 [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)上呼叫 **QueryInterface** 來建立。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-108">The **ITAttributeList** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="cf0d9-109">成員</span><span class="sxs-lookup"><span data-stu-id="cf0d9-109">Members</span></span>

<span data-ttu-id="cf0d9-110">**ITAttributeList** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-110">The **ITAttributeList** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="cf0d9-111">**ITAttributeList** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cf0d9-111">**ITAttributeList** also has these types of members:</span></span>

-   [<span data-ttu-id="cf0d9-112">方法</span><span class="sxs-lookup"><span data-stu-id="cf0d9-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cf0d9-113">方法</span><span class="sxs-lookup"><span data-stu-id="cf0d9-113">Methods</span></span>

<span data-ttu-id="cf0d9-114">**ITAttributeList** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-114">The **ITAttributeList** interface has these methods.</span></span>



| <span data-ttu-id="cf0d9-115">方法</span><span class="sxs-lookup"><span data-stu-id="cf0d9-115">Method</span></span>                                                          | <span data-ttu-id="cf0d9-116">描述</span><span class="sxs-lookup"><span data-stu-id="cf0d9-116">Description</span></span>                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="cf0d9-117">**添加**</span><span class="sxs-lookup"><span data-stu-id="cf0d9-117">**Add**</span></span>](itattributelist-add.md)                              | <span data-ttu-id="cf0d9-118">將屬性加入指定的索引處。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-118">Adds the attribute at the specified index.</span></span><br/>   |
| [<span data-ttu-id="cf0d9-119">**刪除**</span><span class="sxs-lookup"><span data-stu-id="cf0d9-119">**Delete**</span></span>](itattributelist-delete.md)                        | <span data-ttu-id="cf0d9-120">刪除指定索引處的屬性</span><span class="sxs-lookup"><span data-stu-id="cf0d9-120">Deletes the attribute at the specified index</span></span><br/> |
| [<span data-ttu-id="cf0d9-121">**取得 \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="cf0d9-121">**get\_AttributeList**</span></span>](itattributelist-get-attributelist.md) | <span data-ttu-id="cf0d9-122">取得屬性清單。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-122">Gets the list of attributes.</span></span><br/>                 |
| [<span data-ttu-id="cf0d9-123">**取得 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="cf0d9-123">**get\_Count**</span></span>](itattributelist-get-count.md)                 | <span data-ttu-id="cf0d9-124">取得屬性的數目。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-124">Gets the number of attributes.</span></span><br/>               |
| [<span data-ttu-id="cf0d9-125">**取得 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="cf0d9-125">**get\_Item**</span></span>](itattributelist-get-item.md)                   | <span data-ttu-id="cf0d9-126">取得索引所指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-126">Gets the attribute specified by the index.</span></span><br/>   |
| [<span data-ttu-id="cf0d9-127">**put \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="cf0d9-127">**put\_AttributeList**</span></span>](itattributelist-put-attributelist.md) | <span data-ttu-id="cf0d9-128">設定屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="cf0d9-128">Sets the list of attributes.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="cf0d9-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf0d9-129">Requirements</span></span>



| <span data-ttu-id="cf0d9-130">需求</span><span class="sxs-lookup"><span data-stu-id="cf0d9-130">Requirement</span></span> | <span data-ttu-id="cf0d9-131">值</span><span class="sxs-lookup"><span data-stu-id="cf0d9-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0d9-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="cf0d9-132">TAPI version</span></span><br/> | <span data-ttu-id="cf0d9-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="cf0d9-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cf0d9-134">標頭</span><span class="sxs-lookup"><span data-stu-id="cf0d9-134">Header</span></span><br/>       | <dl> <span data-ttu-id="cf0d9-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf0d9-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf0d9-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf0d9-136">Library</span></span><br/>      | <dl> <span data-ttu-id="cf0d9-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="cf0d9-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cf0d9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cf0d9-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="cf0d9-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf0d9-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

