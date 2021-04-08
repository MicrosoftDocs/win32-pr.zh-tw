---
title: 標準字型物件
description: 標準字型物件
ms.assetid: f9b54dc4-24d4-4eb7-b43f-c481d64e52df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0fbe2509dd85c1d15b40dc8008dba60d948b5c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024130"
---
# <a name="standard-font-object"></a><span data-ttu-id="855c1-103">標準字型物件</span><span class="sxs-lookup"><span data-stu-id="855c1-103">Standard Font Object</span></span>

<span data-ttu-id="855c1-104">容器所提供的標準環境字型屬性和控制項提供的標準字型屬性都提供標準的字型物件。</span><span class="sxs-lookup"><span data-stu-id="855c1-104">The standard ambient font property supplied by the container and the standard font property supplied by the control both provide a standard font object.</span></span> <span data-ttu-id="855c1-105">也就是說，這些標準字型提供標準字型物件的 **IDispatch** 指標。</span><span class="sxs-lookup"><span data-stu-id="855c1-105">That is, these standard fonts supply an **IDispatch** pointer to a standard font object.</span></span>

<span data-ttu-id="855c1-106">字型物件是一組系統提供的介面，可在基礎 GDI 字型支援之上執行。</span><span class="sxs-lookup"><span data-stu-id="855c1-106">The font object is a system-provided implementation of a set of interfaces on top of the underlying GDI font support.</span></span> <span data-ttu-id="855c1-107">在給定 [**FONTDESC**](/windows/win32/api/olectl/ns-olectl-fontdesc)結構的情況之下，會透過 API 函數 [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect)來建立字型物件。</span><span class="sxs-lookup"><span data-stu-id="855c1-107">A font object is created through the API function [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect) given a [**FONTDESC**](/windows/win32/api/olectl/ns-olectl-fontdesc) structure.</span></span> <span data-ttu-id="855c1-108">字型物件支援許多讀取/寫入屬性，以及透過其介面 [**>ifont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)的自訂方法，並支援相同的屬性集 (但不支援透過多介面 [**>ifontdisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)) 的方法。</span><span class="sxs-lookup"><span data-stu-id="855c1-108">The font object supports a number of read/write properties as well as custom methods through its interface [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont), and supports the same set of properties (but not the methods) through a dispinterface [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span></span> <span data-ttu-id="855c1-109">介面介面是用於先前所述的字型屬性。</span><span class="sxs-lookup"><span data-stu-id="855c1-109">The dispinterface is used for the font properties mentioned previously.</span></span> <span data-ttu-id="855c1-110">這些屬性會對應至 [**LOGFONT**](/windows/win32/api/dimm/ns-dimm-logfonta) 結構中所描述的 GDI 字型屬性。</span><span class="sxs-lookup"><span data-stu-id="855c1-110">The properties correspond to the GDI font attributes that are described in the [**LOGFONT**](/windows/win32/api/dimm/ns-dimm-logfonta) structure.</span></span>

<span data-ttu-id="855c1-111">字型物件也支援輸出介面 [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) ，讓用戶端可以決定何時會變更字型屬性。</span><span class="sxs-lookup"><span data-stu-id="855c1-111">The font object also supports the outgoing interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) so that a client can determine when font properties change.</span></span> <span data-ttu-id="855c1-112">由於字型物件支援至少一個輸出介面，因此它也會針對此用途來實 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) 和一個用於 **IPropertyNotifySink** 的連接點。</span><span class="sxs-lookup"><span data-stu-id="855c1-112">Since the font object supports at least one outgoing interface, it also implements [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) and one connection point for **IPropertyNotifySink** for this purpose.</span></span>

<span data-ttu-id="855c1-113">字型物件提供的 hFont 屬性是符合為字型指定之其他屬性的 Windows 字型控制碼。</span><span class="sxs-lookup"><span data-stu-id="855c1-113">The font object provides an hFont property that is a Windows font handle that conforms to the other attributes specified for the font.</span></span> <span data-ttu-id="855c1-114">字型物件可能會在可能的情況下延遲實現這個字型，因此在字型上連續設定兩個屬性並不會導致中繼字型被實現。</span><span class="sxs-lookup"><span data-stu-id="855c1-114">The font object delays realizing this font when possible, so consecutively setting two properties on a font won't cause an intermediate font to be realized.</span></span> <span data-ttu-id="855c1-115">此外，作為優化，標準字型物件會維護字型控制碼的快取。</span><span class="sxs-lookup"><span data-stu-id="855c1-115">In addition, as an optimization, the standard font object maintains a cache of font handles.</span></span> <span data-ttu-id="855c1-116">相同進程中具有相同屬性的兩個字型物件將會傳回相同的字型控制碼。</span><span class="sxs-lookup"><span data-stu-id="855c1-116">Two font objects in the same process that have identical properties will return the same font handle.</span></span> <span data-ttu-id="855c1-117">字型物件可以從這個快取中移除字型，這會為使用這個 hFont 屬性的用戶端引進特殊的考慮。</span><span class="sxs-lookup"><span data-stu-id="855c1-117">The font object can remove fonts from this cache at will, which introduces special considerations for clients using this hFont property.</span></span> <span data-ttu-id="855c1-118">如需詳細資訊，請參閱 [**>ifont：： get \_ hFont**](/windows/desktop/api/OCIdl/nf-ocidl-ifont-get_hfont) 。</span><span class="sxs-lookup"><span data-stu-id="855c1-118">See [**IFont::get\_hFont**](/windows/desktop/api/OCIdl/nf-ocidl-ifont-get_hfont) for more details.</span></span>

<span data-ttu-id="855c1-119">字型物件也支援 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ，讓它可以從 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)實例儲存和載入本身。</span><span class="sxs-lookup"><span data-stu-id="855c1-119">The font object also supports [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) such that it can save and load itself from an instance of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="855c1-120">在內部使用字型物件的任何其他物件通常會在物件的持續性處理過程中，儲存並載入字型。</span><span class="sxs-lookup"><span data-stu-id="855c1-120">Any other object that uses a font object internally would normally save and load the font as part of the object's own persistence handling.</span></span>

<span data-ttu-id="855c1-121">此外，字型物件支援 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) ，它會提供一個屬性集，其中包含每個字型屬性的具類型值。</span><span class="sxs-lookup"><span data-stu-id="855c1-121">In addition, the font object supports [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) through which it provides a property set containing typed values for each font property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="855c1-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="855c1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="855c1-123">控制項屬性</span><span class="sxs-lookup"><span data-stu-id="855c1-123">Control Properties</span></span>](control-properties.md)
</dt> </dl>

 

 