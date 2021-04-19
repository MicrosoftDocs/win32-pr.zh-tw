---
description: 由應用程式用來列舉專案樹狀結構目前資料夾中的 IWiaItem2 物件。
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: 'IEnumWiaItem2 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972466"
---
# <a name="ienumwiaitem2-interface"></a><span data-ttu-id="3ccc9-103">IEnumWiaItem2 介面</span><span class="sxs-lookup"><span data-stu-id="3ccc9-103">IEnumWiaItem2 interface</span></span>

<span data-ttu-id="3ccc9-104">由應用程式用來列舉專案樹狀結構目前資料夾中的 [**IWiaItem2**](-wia-iwiaitem2.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3ccc9-104">Used by applications to enumerate [**IWiaItem2**](-wia-iwiaitem2.md) objects in the item tree's current folder.</span></span>

## <a name="members"></a><span data-ttu-id="3ccc9-105">成員</span><span class="sxs-lookup"><span data-stu-id="3ccc9-105">Members</span></span>

<span data-ttu-id="3ccc9-106">**IEnumWiaItem2** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="3ccc9-106">The **IEnumWiaItem2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3ccc9-107">**IEnumWiaItem2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3ccc9-107">**IEnumWiaItem2** also has these types of members:</span></span>

-   [<span data-ttu-id="3ccc9-108">方法</span><span class="sxs-lookup"><span data-stu-id="3ccc9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3ccc9-109">方法</span><span class="sxs-lookup"><span data-stu-id="3ccc9-109">Methods</span></span>

<span data-ttu-id="3ccc9-110">**IEnumWiaItem2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3ccc9-110">The **IEnumWiaItem2** interface has these methods.</span></span>



| <span data-ttu-id="3ccc9-111">方法</span><span class="sxs-lookup"><span data-stu-id="3ccc9-111">Method</span></span>                                          | <span data-ttu-id="3ccc9-112">描述</span><span class="sxs-lookup"><span data-stu-id="3ccc9-112">Description</span></span>                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ccc9-113">**克隆**</span><span class="sxs-lookup"><span data-stu-id="3ccc9-113">**Clone**</span></span>](-wia-ienumwiaitem2-clone.md)       | <span data-ttu-id="3ccc9-114">建立 **IEnumWiaItem2** 介面的其他實例，並將指標傳回給它。</span><span class="sxs-lookup"><span data-stu-id="3ccc9-114">Creates an additional instance of the **IEnumWiaItem2** interface and sends back a pointer to it.</span></span> <br/>                  |
| [<span data-ttu-id="3ccc9-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="3ccc9-115">**GetCount**</span></span>](-wia-ienumwiaitem2-getcount.md) | <span data-ttu-id="3ccc9-116">傳回這個列舉值所儲存的元素數目。</span><span class="sxs-lookup"><span data-stu-id="3ccc9-116">Returns the number of elements stored by this enumerator.</span></span> <br/>                                                          |
| [<span data-ttu-id="3ccc9-117">**下一步**</span><span class="sxs-lookup"><span data-stu-id="3ccc9-117">**Next**</span></span>](-wia-ienumwiaitem2-next.md)         | <span data-ttu-id="3ccc9-118">填滿 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="3ccc9-118">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="3ccc9-119">**重設**</span><span class="sxs-lookup"><span data-stu-id="3ccc9-119">**Reset**</span></span>](-wia-ienumwiaitem2-reset.md)       | <span data-ttu-id="3ccc9-120">將列舉參考重設為第一個 [**IWiaItem2**](-wia-iwiaitem2.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3ccc9-120">Resets the enumeration reference to the first [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <br/>                          |
| [<span data-ttu-id="3ccc9-121">**跳過**</span><span class="sxs-lookup"><span data-stu-id="3ccc9-121">**Skip**</span></span>](-wia-ienumwiaitem2-skip.md)         | <span data-ttu-id="3ccc9-122">在列舉可用的 [**IWiaItem2**](-wia-iwiaitem2.md) 物件期間略過指定數目的專案。</span><span class="sxs-lookup"><span data-stu-id="3ccc9-122">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3ccc9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ccc9-123">Requirements</span></span>



| <span data-ttu-id="3ccc9-124">需求</span><span class="sxs-lookup"><span data-stu-id="3ccc9-124">Requirement</span></span> | <span data-ttu-id="3ccc9-125">值</span><span class="sxs-lookup"><span data-stu-id="3ccc9-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ccc9-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ccc9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3ccc9-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ccc9-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3ccc9-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ccc9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3ccc9-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ccc9-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3ccc9-130">標頭</span><span class="sxs-lookup"><span data-stu-id="3ccc9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ccc9-131"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="3ccc9-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ccc9-132">Idl</span><span class="sxs-lookup"><span data-stu-id="3ccc9-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ccc9-133"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ccc9-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
