---
description: IWiaTransfer 介面會提供資料流程傳輸的資料。
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: 'IWiaTransfer 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191395"
---
# <a name="iwiatransfer-interface"></a><span data-ttu-id="2dfaa-103">IWiaTransfer 介面</span><span class="sxs-lookup"><span data-stu-id="2dfaa-103">IWiaTransfer interface</span></span>

<span data-ttu-id="2dfaa-104">**IWiaTransfer** 介面會提供資料流程傳輸的資料。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-104">The **IWiaTransfer** interface provides stream-based transfer of data.</span></span>

## <a name="members"></a><span data-ttu-id="2dfaa-105">成員</span><span class="sxs-lookup"><span data-stu-id="2dfaa-105">Members</span></span>

<span data-ttu-id="2dfaa-106">**IWiaTransfer** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-106">The **IWiaTransfer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2dfaa-107">**IWiaTransfer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2dfaa-107">**IWiaTransfer** also has these types of members:</span></span>

-   [<span data-ttu-id="2dfaa-108">方法</span><span class="sxs-lookup"><span data-stu-id="2dfaa-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2dfaa-109">方法</span><span class="sxs-lookup"><span data-stu-id="2dfaa-109">Methods</span></span>

<span data-ttu-id="2dfaa-110">**IWiaTransfer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-110">The **IWiaTransfer** interface has these methods.</span></span>



| <span data-ttu-id="2dfaa-111">方法</span><span class="sxs-lookup"><span data-stu-id="2dfaa-111">Method</span></span>                                                                 | <span data-ttu-id="2dfaa-112">描述</span><span class="sxs-lookup"><span data-stu-id="2dfaa-112">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dfaa-113">**取消**</span><span class="sxs-lookup"><span data-stu-id="2dfaa-113">**Cancel**</span></span>](-wia-iwiatransfer-cancel.md)                             | <span data-ttu-id="2dfaa-114">取消目前的傳送作業。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-114">Cancels the current transfer operation.</span></span> <br/>                                         |
| [<span data-ttu-id="2dfaa-115">**下載**</span><span class="sxs-lookup"><span data-stu-id="2dfaa-115">**Download**</span></span>](-wia-iwiatransfer-download.md)                         | <span data-ttu-id="2dfaa-116">起始將資料下載至呼叫端。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-116">Initiates a data download to the caller.</span></span> <br/>                                        |
| [<span data-ttu-id="2dfaa-117">**EnumWIA \_ 格式 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="2dfaa-117">**EnumWIA\_FORMAT\_INFO**</span></span>](-wia-iwiatransfer-enumwia-format-info.md) | <span data-ttu-id="2dfaa-118">針對 WIA 2.0 裝置支援的傳輸格式建立枚舉器。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-118">Creates an enumerator for the transfer formats that the WIA 2.0 device supports.</span></span><br/> |
| [<span data-ttu-id="2dfaa-119">**上傳**</span><span class="sxs-lookup"><span data-stu-id="2dfaa-119">**Upload**</span></span>](-wia-iwiatransfer-upload.md)                             | <span data-ttu-id="2dfaa-120">從呼叫端起始單一專案的資料上傳。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-120">Initiates a data upload of a single item from the caller.</span></span> <br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="2dfaa-121">備註</span><span class="sxs-lookup"><span data-stu-id="2dfaa-121">Remarks</span></span>

<span data-ttu-id="2dfaa-122">**IWiaTransfer** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-122">The **IWiaTransfer** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="2dfaa-123">IUnknown 方法</span><span class="sxs-lookup"><span data-stu-id="2dfaa-123">IUnknown Methods</span></span>                                        | <span data-ttu-id="2dfaa-124">Description</span><span class="sxs-lookup"><span data-stu-id="2dfaa-124">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="2dfaa-125">[IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="2dfaa-125">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="2dfaa-126">傳回受支援介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-126">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="2dfaa-127">IUnknown：： AddRef</span><span class="sxs-lookup"><span data-stu-id="2dfaa-127">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="2dfaa-128">遞增參考次數。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-128">Increments reference count.</span></span>               |
| [<span data-ttu-id="2dfaa-129">IUnknown：： Release</span><span class="sxs-lookup"><span data-stu-id="2dfaa-129">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="2dfaa-130">遞減參考次數。</span><span class="sxs-lookup"><span data-stu-id="2dfaa-130">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="2dfaa-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dfaa-131">Requirements</span></span>



| <span data-ttu-id="2dfaa-132">需求</span><span class="sxs-lookup"><span data-stu-id="2dfaa-132">Requirement</span></span> | <span data-ttu-id="2dfaa-133">值</span><span class="sxs-lookup"><span data-stu-id="2dfaa-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dfaa-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2dfaa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2dfaa-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2dfaa-135">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2dfaa-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2dfaa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2dfaa-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2dfaa-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2dfaa-138">標頭</span><span class="sxs-lookup"><span data-stu-id="2dfaa-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dfaa-139"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="2dfaa-139"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="2dfaa-140">Idl</span><span class="sxs-lookup"><span data-stu-id="2dfaa-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2dfaa-141"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2dfaa-141"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="2dfaa-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="2dfaa-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="2dfaa-143"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2dfaa-143"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
