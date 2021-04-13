---
description: IWiaTransferCallback 介面會在資料傳輸期間接收回呼。
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: 'IWiaTransferCallback 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113293"
---
# <a name="iwiatransfercallback-interface"></a><span data-ttu-id="041a0-103">IWiaTransferCallback 介面</span><span class="sxs-lookup"><span data-stu-id="041a0-103">IWiaTransferCallback interface</span></span>

<span data-ttu-id="041a0-104">**IWiaTransferCallback** 介面會在資料傳輸期間接收回呼。</span><span class="sxs-lookup"><span data-stu-id="041a0-104">The **IWiaTransferCallback** interface receives callbacks during a data transfer.</span></span>

## <a name="members"></a><span data-ttu-id="041a0-105">成員</span><span class="sxs-lookup"><span data-stu-id="041a0-105">Members</span></span>

<span data-ttu-id="041a0-106">**IWiaTransferCallback** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="041a0-106">The **IWiaTransferCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="041a0-107">**IWiaTransferCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="041a0-107">**IWiaTransferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="041a0-108">方法</span><span class="sxs-lookup"><span data-stu-id="041a0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="041a0-109">方法</span><span class="sxs-lookup"><span data-stu-id="041a0-109">Methods</span></span>

<span data-ttu-id="041a0-110">**IWiaTransferCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="041a0-110">The **IWiaTransferCallback** interface has these methods.</span></span>



| <span data-ttu-id="041a0-111">方法</span><span class="sxs-lookup"><span data-stu-id="041a0-111">Method</span></span>                                                                 | <span data-ttu-id="041a0-112">描述</span><span class="sxs-lookup"><span data-stu-id="041a0-112">Description</span></span>                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="041a0-113">**GetNextStream**</span><span class="sxs-lookup"><span data-stu-id="041a0-113">**GetNextStream**</span></span>](-wia-iwiatransfercallback-getnextstream.md)       | <span data-ttu-id="041a0-114">取得指定之專案的新資料流程。</span><span class="sxs-lookup"><span data-stu-id="041a0-114">Gets a new stream for the specified item.</span></span> <br/>                    |
| [<span data-ttu-id="041a0-115">**TransferCallback**</span><span class="sxs-lookup"><span data-stu-id="041a0-115">**TransferCallback**</span></span>](-wia-iwiatransfercallback-transfercallback.md) | <span data-ttu-id="041a0-116">提供傳輸期間的進度和其他通知。</span><span class="sxs-lookup"><span data-stu-id="041a0-116">Provides progress and other notifications during a transfer.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="041a0-117">備註</span><span class="sxs-lookup"><span data-stu-id="041a0-117">Remarks</span></span>

<span data-ttu-id="041a0-118">影像處理篩選器開發人員應該執行這個介面和 [**IWiaImageFilter**](-wia-iwiaimagefilter.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="041a0-118">Image processing filter developers should implement this interface and the [**IWiaImageFilter**](-wia-iwiaimagefilter.md) interface.</span></span>

<span data-ttu-id="041a0-119">**IWiaTransferCallback** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。</span><span class="sxs-lookup"><span data-stu-id="041a0-119">The **IWiaTransferCallback** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="041a0-120">IUnknown 方法</span><span class="sxs-lookup"><span data-stu-id="041a0-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="041a0-121">Description</span><span class="sxs-lookup"><span data-stu-id="041a0-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="041a0-122">[IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="041a0-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="041a0-123">傳回受支援介面的指標。</span><span class="sxs-lookup"><span data-stu-id="041a0-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="041a0-124">IUnknown：： AddRef</span><span class="sxs-lookup"><span data-stu-id="041a0-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="041a0-125">遞增參考次數。</span><span class="sxs-lookup"><span data-stu-id="041a0-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="041a0-126">IUnknown：： Release</span><span class="sxs-lookup"><span data-stu-id="041a0-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="041a0-127">遞減參考次數。</span><span class="sxs-lookup"><span data-stu-id="041a0-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="041a0-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="041a0-128">Requirements</span></span>



| <span data-ttu-id="041a0-129">需求</span><span class="sxs-lookup"><span data-stu-id="041a0-129">Requirement</span></span> | <span data-ttu-id="041a0-130">值</span><span class="sxs-lookup"><span data-stu-id="041a0-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="041a0-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="041a0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="041a0-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="041a0-132">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="041a0-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="041a0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="041a0-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="041a0-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="041a0-135">標頭</span><span class="sxs-lookup"><span data-stu-id="041a0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="041a0-136"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="041a0-136"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="041a0-137">Idl</span><span class="sxs-lookup"><span data-stu-id="041a0-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="041a0-138"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="041a0-138"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="041a0-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="041a0-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="041a0-140"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="041a0-140"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
