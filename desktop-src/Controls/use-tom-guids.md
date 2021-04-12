---
title: 如何使用 TOM Guid
description: 在 MIDL 介面語句內的 Tom 中，會提供文字物件模型 (TOM) Guid \_ 。 若要使用相關聯的介面，您必須先使用 GUID 宣告介面。
ms.assetid: 48FF98C9-D42E-4E7F-874F-8E56F730E24E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c937d8b3c3612a3a49f27f18ac7c392b7a596
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "104462812"
---
# <a name="how-to-use-tom-guids"></a><span data-ttu-id="476d6-104">如何使用 TOM Guid</span><span class="sxs-lookup"><span data-stu-id="476d6-104">How to Use TOM GUIDs</span></span>

<span data-ttu-id="476d6-105">在 MIDL 介面語句內的 Tom 中，會提供文字物件模型 (TOM) Guid \_ 。</span><span class="sxs-lookup"><span data-stu-id="476d6-105">Text Object Model (TOM) GUIDs are given in Tom.h inside the MIDL\_INTERFACE statements.</span></span> <span data-ttu-id="476d6-106">若要使用相關聯的介面，您必須先使用 GUID 宣告介面。</span><span class="sxs-lookup"><span data-stu-id="476d6-106">To use the associated interfaces, you must first declare the interface by using the GUID.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="476d6-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="476d6-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="476d6-108">技術</span><span class="sxs-lookup"><span data-stu-id="476d6-108">Technologies</span></span>

-   [<span data-ttu-id="476d6-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="476d6-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="476d6-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="476d6-110">Prerequisites</span></span>

-   <span data-ttu-id="476d6-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="476d6-111">C/C++</span></span>
-   <span data-ttu-id="476d6-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="476d6-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="476d6-113">指示</span><span class="sxs-lookup"><span data-stu-id="476d6-113">Instructions</span></span>

### <a name="use-a-tom-guid"></a><span data-ttu-id="476d6-114">使用 TOM GUID</span><span class="sxs-lookup"><span data-stu-id="476d6-114">Use a TOM GUID</span></span>

<span data-ttu-id="476d6-115">下列範例程式碼示範如何使用 [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) 介面。</span><span class="sxs-lookup"><span data-stu-id="476d6-115">The following example code demonstrates how to use the [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) interface.</span></span>


```C++
#define DEFINE_GUIDXXX(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8) \
        EXTERN_C const GUID CDECL name \
                = { l, w1, w2, { b1, b2,  b3,  b4,  b5,  b6,  b7,  b8 } }

DEFINE_GUIDXXX(IID_ITextDocument,0x8CC497C0,0xA1DF,0x11CE,0x80,0x98,
                0x00,0xAA,0x00,0x47,0xBE,0x5D);
```



## <a name="related-topics"></a><span data-ttu-id="476d6-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="476d6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="476d6-117">使用 Text 物件模型</span><span class="sxs-lookup"><span data-stu-id="476d6-117">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="476d6-118">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="476d6-118">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="476d6-119">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="476d6-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




