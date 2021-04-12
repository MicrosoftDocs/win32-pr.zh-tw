---
description: 當應用程式在任何可寫入的 Windows 映像取得 (WIA) 屬性上執行 IPropertyStorage：： WriteMultiple 作業時，WIA 驅動程式會在新的屬性值上執行驗證。
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: WIA 屬性驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191384"
---
# <a name="wia-property-validation"></a><span data-ttu-id="1126d-103">WIA 屬性驗證</span><span class="sxs-lookup"><span data-stu-id="1126d-103">WIA Property Validation</span></span>

<span data-ttu-id="1126d-104">當應用程式在任何可寫入的 Windows 映像取得 (WIA) 屬性上執行 [IPropertyStorage：： WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) 作業時，wia 驅動程式會在新的屬性值上執行驗證。</span><span class="sxs-lookup"><span data-stu-id="1126d-104">When an application performs an [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation on any writeable Windows Image Acquisition (WIA) property, the WIA driver performs a validation on the new property value.</span></span> <span data-ttu-id="1126d-105">寫入一個屬性可能會影響變更其他屬性值的副作用。</span><span class="sxs-lookup"><span data-stu-id="1126d-105">Writing one property may have side affects that change other property values.</span></span> <span data-ttu-id="1126d-106">在寫入作業之後，應用程式會讀取所有屬性值，以判斷所有屬性都設定為應用程式所需的值。</span><span class="sxs-lookup"><span data-stu-id="1126d-106">It is up to the application to read all property values after a write operation to determine that all properties are set to values the application desires.</span></span>

<span data-ttu-id="1126d-107">您可以使用 [IPropertyStorage：： WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) 作業同時寫入多個屬性。</span><span class="sxs-lookup"><span data-stu-id="1126d-107">Multiple properties can be written simultaneously using the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation.</span></span> <span data-ttu-id="1126d-108">在某些情況下，某些屬性指派會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="1126d-108">There may be cases where some property assignments conflict.</span></span> <span data-ttu-id="1126d-109">在這種情況下，用來解決衝突的優先順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="1126d-109">In such cases, the priority used to resolve conflicts is as follows:</span></span>

1.  <span data-ttu-id="1126d-110">WIA \_ IP 的 \_ 當前 \_ 意圖</span><span class="sxs-lookup"><span data-stu-id="1126d-110">WIA\_IPS\_CUR\_INTENT</span></span>
2.  <span data-ttu-id="1126d-111">WIA \_ IPA \_ 資料類型</span><span class="sxs-lookup"><span data-stu-id="1126d-111">WIA\_IPA\_DATATYPE</span></span>
3.  <span data-ttu-id="1126d-112">WIA \_ IPA \_ 深度</span><span class="sxs-lookup"><span data-stu-id="1126d-112">WIA\_IPA\_DEPTH</span></span>
4.  <span data-ttu-id="1126d-113">WIA \_ IP \_ XRES</span><span class="sxs-lookup"><span data-stu-id="1126d-113">WIA\_IPS\_XRES</span></span>
5.  <span data-ttu-id="1126d-114">WIA \_ IP \_ YRES</span><span class="sxs-lookup"><span data-stu-id="1126d-114">WIA\_IPS\_YRES</span></span>
6.  <span data-ttu-id="1126d-115">WIA \_ IP \_ XPOS</span><span class="sxs-lookup"><span data-stu-id="1126d-115">WIA\_IPS\_XPOS</span></span>
7.  <span data-ttu-id="1126d-116">WIA \_ IP \_ YPOS</span><span class="sxs-lookup"><span data-stu-id="1126d-116">WIA\_IPS\_YPOS</span></span>
8.  <span data-ttu-id="1126d-117">WIA \_ IP \_ 範圍</span><span class="sxs-lookup"><span data-stu-id="1126d-117">WIA\_IPS\_XEXTENT</span></span>
9.  <span data-ttu-id="1126d-118">WIA \_ IP \_ YEXTENT</span><span class="sxs-lookup"><span data-stu-id="1126d-118">WIA\_IPS\_YEXTENT</span></span>

## <a name="related-topics"></a><span data-ttu-id="1126d-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="1126d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1126d-120">**IWiaPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="1126d-120">**IWiaPropertyStorage**</span></span>](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
