---
description: IWiaErrorHandler 介面會提供方法來處理應用程式要求影像資料時可能發生的錯誤（不論是預覽或最終位）。
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: 'IWiaErrorHandler 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113896"
---
# <a name="iwiaerrorhandler-interface"></a><span data-ttu-id="3c2ae-103">IWiaErrorHandler 介面</span><span class="sxs-lookup"><span data-stu-id="3c2ae-103">IWiaErrorHandler interface</span></span>

<span data-ttu-id="3c2ae-104">**IWiaErrorHandler** 介面會提供方法來處理應用程式要求影像資料時可能發生的錯誤（不論是預覽或最終位）。</span><span class="sxs-lookup"><span data-stu-id="3c2ae-104">The **IWiaErrorHandler** interface provides methods to handle errors that may occur when an application requests image data, whether for preview or final bits.</span></span>

## <a name="members"></a><span data-ttu-id="3c2ae-105">成員</span><span class="sxs-lookup"><span data-stu-id="3c2ae-105">Members</span></span>

<span data-ttu-id="3c2ae-106">**IWiaErrorHandler** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="3c2ae-106">The **IWiaErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3c2ae-107">**IWiaErrorHandler** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3c2ae-107">**IWiaErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="3c2ae-108">方法</span><span class="sxs-lookup"><span data-stu-id="3c2ae-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3c2ae-109">方法</span><span class="sxs-lookup"><span data-stu-id="3c2ae-109">Methods</span></span>

<span data-ttu-id="3c2ae-110">**IWiaErrorHandler** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3c2ae-110">The **IWiaErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="3c2ae-111">方法</span><span class="sxs-lookup"><span data-stu-id="3c2ae-111">Method</span></span>                                                                     | <span data-ttu-id="3c2ae-112">描述</span><span class="sxs-lookup"><span data-stu-id="3c2ae-112">Description</span></span>                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c2ae-113">**GetStatusDescription**</span><span class="sxs-lookup"><span data-stu-id="3c2ae-113">**GetStatusDescription**</span></span>](-wia-iwiaerrorhandler-getstatusdescription.md) | <span data-ttu-id="3c2ae-114">傳回描述狀態碼的字串。</span><span class="sxs-lookup"><span data-stu-id="3c2ae-114">Returns a string that describes the status code.</span></span><br/>                                             |
| [<span data-ttu-id="3c2ae-115">**ReportStatus**</span><span class="sxs-lookup"><span data-stu-id="3c2ae-115">**ReportStatus**</span></span>](-wia-iwiaerrorhandler-reportstatus.md)                 | <span data-ttu-id="3c2ae-116">處理影像資料傳輸期間的狀態和錯誤訊息，並將其顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="3c2ae-116">Handles status and error messages during image data transfers and displays them to the user.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c2ae-117">備註</span><span class="sxs-lookup"><span data-stu-id="3c2ae-117">Remarks</span></span>

<span data-ttu-id="3c2ae-118">應用程式回呼物件可以執行 **IWiaErrorHandler**。</span><span class="sxs-lookup"><span data-stu-id="3c2ae-118">The application callback object can implement **IWiaErrorHandler**.</span></span>

<span data-ttu-id="3c2ae-119">此介面並非設計用來處理在影像資料傳輸之外發生的錯誤，例如，取得或設定裝置屬性或 unreturned 回呼至驅動程式時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3c2ae-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2ae-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c2ae-120">Requirements</span></span>



| <span data-ttu-id="3c2ae-121">需求</span><span class="sxs-lookup"><span data-stu-id="3c2ae-121">Requirement</span></span> | <span data-ttu-id="3c2ae-122">值</span><span class="sxs-lookup"><span data-stu-id="3c2ae-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2ae-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c2ae-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2ae-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c2ae-124">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3c2ae-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c2ae-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2ae-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c2ae-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3c2ae-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3c2ae-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c2ae-128"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ae-128"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="3c2ae-129">Idl</span><span class="sxs-lookup"><span data-stu-id="3c2ae-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c2ae-130"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ae-130"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="3c2ae-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c2ae-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c2ae-132"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ae-132"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
