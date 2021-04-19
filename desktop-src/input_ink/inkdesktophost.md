---
description: 實行 IInkDesktopHost 介面。
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: InkDesktopHost 類別
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: d5dac80a4ee09bb4b78a4d61ca0efa74e99babb9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "106974753"
---
# <a name="inkdesktophost-class"></a><span data-ttu-id="1873f-103">InkDesktopHost 類別</span><span class="sxs-lookup"><span data-stu-id="1873f-103">InkDesktopHost class</span></span>

<span data-ttu-id="1873f-104">實行 [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) 介面。</span><span class="sxs-lookup"><span data-stu-id="1873f-104">Implements the [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) interface.</span></span>

<span data-ttu-id="1873f-105">[**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)物件可讓您透過建立應用程式執行緒來進行筆跡輸入、處理和轉譯，以裝載 [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)物件，並將它插入應用程式的 [DirectComposition](../directcomp/directcomposition-portal.md)視覺化樹狀結構中。</span><span class="sxs-lookup"><span data-stu-id="1873f-105">An [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) object enables ink input, processing, and rendering through the creation of an app thread to host an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object and insert it into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

## <a name="members"></a><span data-ttu-id="1873f-106">成員</span><span class="sxs-lookup"><span data-stu-id="1873f-106">Members</span></span>

<span data-ttu-id="1873f-107">**InkDesktopHost** 類別繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="1873f-107">The **InkDesktopHost** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1873f-108">**InkDesktopHost** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1873f-108">**InkDesktopHost** also has these types of members:</span></span>

- [<span data-ttu-id="1873f-109">方法</span><span class="sxs-lookup"><span data-stu-id="1873f-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1873f-110">方法</span><span class="sxs-lookup"><span data-stu-id="1873f-110">Methods</span></span>

<span data-ttu-id="1873f-111">**InkDesktopHost** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1873f-111">The **InkDesktopHost** class has these methods.</span></span>

| <span data-ttu-id="1873f-112">方法</span><span class="sxs-lookup"><span data-stu-id="1873f-112">Method</span></span> | <span data-ttu-id="1873f-113">描述</span><span class="sxs-lookup"><span data-stu-id="1873f-113">Description</span></span> |
|---|---|
| [<span data-ttu-id="1873f-114">**CreateAndInitializeInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="1873f-114">**CreateAndInitializeInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | <span data-ttu-id="1873f-115">在應用程式執行緒上建立 [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) 物件，並將它連接至應用程式的 [DirectComposition](../directcomp/directcomposition-portal.md) 視覺化樹狀結構，並設定物件的大小。</span><span class="sxs-lookup"><span data-stu-id="1873f-115">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread, connects it to the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree, and sets the size of the object.</span></span><br/> |
| [<span data-ttu-id="1873f-116">**CreateInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="1873f-116">**CreateInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | <span data-ttu-id="1873f-117">在應用程式執行緒上建立 [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) 物件。</span><span class="sxs-lookup"><span data-stu-id="1873f-117">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread.</span></span><br/> |
| [<span data-ttu-id="1873f-118">**QueueWorkItem**</span><span class="sxs-lookup"><span data-stu-id="1873f-118">**QueueWorkItem**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | <span data-ttu-id="1873f-119">將筆墨作業加入到工作佇列中，以便在 **InkDesktopHost** 執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="1873f-119">Add an ink operation to a work queue for execution on the **InkDesktopHost** thread.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="1873f-120">建立 \\ 存取函數</span><span class="sxs-lookup"><span data-stu-id="1873f-120">Creation\\Access Functions</span></span>

<span data-ttu-id="1873f-121">使用類別識別碼<strong>InkDesktopHost</strong>呼叫[<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得物件的參考。</span><span class="sxs-lookup"><span data-stu-id="1873f-121">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkDesktopHost</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&amp;_spInkHost));
```

## <a name="requirements"></a><span data-ttu-id="1873f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1873f-122">Requirements</span></span>

| <span data-ttu-id="1873f-123">需求</span><span class="sxs-lookup"><span data-stu-id="1873f-123">Requirement</span></span> | <span data-ttu-id="1873f-124">值</span><span class="sxs-lookup"><span data-stu-id="1873f-124">Value</span></span> |
|---|---|
| <span data-ttu-id="1873f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1873f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1873f-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1873f-126">Windows 10 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1873f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1873f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1873f-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="1873f-128">None supported</span></span><br/> |
| <span data-ttu-id="1873f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="1873f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1873f-130"><dt>InkPresenterDesktop。h</dt></span><span class="sxs-lookup"><span data-stu-id="1873f-130"><dt>InkPresenterDesktop.h</dt></span></span> </dl>   |
| <span data-ttu-id="1873f-131">Idl</span><span class="sxs-lookup"><span data-stu-id="1873f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1873f-132"><dt>InkPresenterDesktop .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1873f-132"><dt>InkPresenterDesktop.idl</dt></span></span> </dl> |
| <span data-ttu-id="1873f-133">IID</span><span class="sxs-lookup"><span data-stu-id="1873f-133">IID</span></span><br/>                      | <span data-ttu-id="1873f-134">IID \_ IInkDesktopHost 定義為4ce7d875-a981-4140-a1ff-ad93258e8d59</span><span class="sxs-lookup"><span data-stu-id="1873f-134">IID\_IInkDesktopHost is defined as 4ce7d875-a981-4140-a1ff-ad93258e8d59</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="1873f-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="1873f-135">Related topics</span></span>

<span data-ttu-id="1873f-136">[筆跡展示者類別](ink-presenter-classes.md)、[畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)、[筆墨分析範例](/samples/microsoft/windows-universal-samples/inkanalysis/)、[簡單筆墨範例](/samples/microsoft/windows-universal-samples/simpleink/)、[複雜](/samples/microsoft/windows-universal-samples/complexink/)的筆墨範例</span><span class="sxs-lookup"><span data-stu-id="1873f-136">[Ink presenter classes](ink-presenter-classes.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
