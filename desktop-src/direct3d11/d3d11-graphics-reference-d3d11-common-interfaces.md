---
title: 一般版本介面
description: 本節包含通用版本介面的相關資訊。
ms.assetid: d228c3c2-e2ff-4723-aec1-5c3ce82c321d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f535650fa24593cc4b663c1a2b01a1a2d53a9b3b
ms.sourcegitcommit: 8f833c83be1accc119cc57e67b608ffe1e0159b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/07/2020
ms.locfileid: "103684203"
---
# <a name="common-version-interfaces"></a><span data-ttu-id="773fe-103">一般版本介面</span><span class="sxs-lookup"><span data-stu-id="773fe-103">Common version interfaces</span></span>

<span data-ttu-id="773fe-104">本節包含通用版本介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="773fe-104">This section contains information about the common version interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="773fe-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="773fe-105">In this section</span></span>

| <span data-ttu-id="773fe-106">主題</span><span class="sxs-lookup"><span data-stu-id="773fe-106">Topic</span></span> | <span data-ttu-id="773fe-107">描述</span><span class="sxs-lookup"><span data-stu-id="773fe-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="773fe-108">**ID3D10Blob**</span><span class="sxs-lookup"><span data-stu-id="773fe-108">**ID3D10Blob**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3d10blob) | <span data-ttu-id="773fe-109">這個介面是用來傳回任意長度的資料。</span><span class="sxs-lookup"><span data-stu-id="773fe-109">This interface is used to return arbitrary-length data.</span></span> |
| <span data-ttu-id="773fe-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="773fe-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span> | <span data-ttu-id="773fe-111">這個介面是用來傳回任意長度的資料。</span><span class="sxs-lookup"><span data-stu-id="773fe-111">This interface is used to return data of arbitrary length.</span></span> |
| [<span data-ttu-id="773fe-112">**ID3DDestructionNotifier**</span><span class="sxs-lookup"><span data-stu-id="773fe-112">**ID3DDestructionNotifier**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier) | <span data-ttu-id="773fe-113">當直接 3D nano COM 物件終結時，用來註冊回呼。</span><span class="sxs-lookup"><span data-stu-id="773fe-113">Used to register for callbacks when a Direct 3D nano-COM object is destroyed.</span></span> |
| [<span data-ttu-id="773fe-114">**ID3DInclude**</span><span class="sxs-lookup"><span data-stu-id="773fe-114">**ID3DInclude**</span></span>](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) | <span data-ttu-id="773fe-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) 是使用者所執行的 include 介面，可讓應用程式呼叫使用者可覆寫的方法，以開啟和關閉著色器的 \# 包含檔案。</span><span class="sxs-lookup"><span data-stu-id="773fe-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader \#include files.</span></span> |
| [<span data-ttu-id="773fe-116">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="773fe-116">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) | <span data-ttu-id="773fe-117">[**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation)介面可讓應用程式描述應用程式程式碼流程內的概念區段和標記。</span><span class="sxs-lookup"><span data-stu-id="773fe-117">The [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) interface enables an application to describe conceptual sections and markers within the application's code flow.</span></span> <span data-ttu-id="773fe-118">經過適當啟用的工具（例如 Microsoft Visual Studio Ultimate 2012）可以在工具的 Microsoft Direct3D 時間表上以視覺化方式顯示這些區段和標記，而此工具會將應用程式進行調試。</span><span class="sxs-lookup"><span data-stu-id="773fe-118">An appropriately enabled tool, such as Microsoft Visual Studio Ultimate 2012, can display these sections and markers visually along the tool's Microsoft Direct3D time line, while the tool debugs the application.</span></span> <span data-ttu-id="773fe-119">這些視覺效果附注可讓這類工具的使用者導覽到感興趣的時間行部分，或瞭解應用程式程式碼的某些區段所產生的 Direct3D 呼叫集合。</span><span class="sxs-lookup"><span data-stu-id="773fe-119">These visual notes allow users of such a tool to navigate to parts of the time line that are of interest, or to understand what set of Direct3D calls are produced by certain sections of the application's code.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="773fe-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="773fe-120">Related topics</span></span>

[<span data-ttu-id="773fe-121">一般版本參考</span><span class="sxs-lookup"><span data-stu-id="773fe-121">Common version reference</span></span>](d3d11-graphics-reference-d3d11-common.md)
