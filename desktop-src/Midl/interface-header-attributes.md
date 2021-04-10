---
title: 介面標頭屬性
description: 將這些屬性併入介面標頭中，以傳達整個介面的相關資訊。
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL MIDL、屬性、介面標頭
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021254"
---
# <a name="interface-header-attributes"></a><span data-ttu-id="4e247-104">介面標頭屬性</span><span class="sxs-lookup"><span data-stu-id="4e247-104">Interface Header Attributes</span></span>

<span data-ttu-id="4e247-105">將這些屬性併入介面標頭中，以傳達整個介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4e247-105">Incorporate these attributes in the interface header to convey information about the entire interface.</span></span>



| <span data-ttu-id="4e247-106">屬性</span><span class="sxs-lookup"><span data-stu-id="4e247-106">Attribute</span></span>                                   | <span data-ttu-id="4e247-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="4e247-107">Usage</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e247-108">**非同步 \_ uuid**</span><span class="sxs-lookup"><span data-stu-id="4e247-108">**async\_uuid**</span></span>](async-uuid.md)           | <span data-ttu-id="4e247-109">指示 MIDL 編譯器定義 COM 介面的同步和非同步版本。</span><span class="sxs-lookup"><span data-stu-id="4e247-109">Directs the MIDL compiler to define both synchronous and asynchronous versions of a COM interface.</span></span>                                                                                                                                               |
| [<span data-ttu-id="4e247-110">**uuid**</span><span class="sxs-lookup"><span data-stu-id="4e247-110">**uuid**</span></span>](uuid.md)                        | <span data-ttu-id="4e247-111">指定可區分特定介面與其他介面的128位值。</span><span class="sxs-lookup"><span data-stu-id="4e247-111">Designates a 128-bit value that distinguishes a particular interface from all others.</span></span> <span data-ttu-id="4e247-112">實際值可能代表 GUID、CLSID 或 IID。</span><span class="sxs-lookup"><span data-stu-id="4e247-112">The actual value may represent a GUID, a CLSID, or an IID.</span></span>                                                                                                 |
| [<span data-ttu-id="4e247-113">**當地**</span><span class="sxs-lookup"><span data-stu-id="4e247-113">**local**</span></span>](local.md)                      | <span data-ttu-id="4e247-114">指示 MIDL 編譯器只產生標頭檔。</span><span class="sxs-lookup"><span data-stu-id="4e247-114">Directs the MIDL compiler to generate header files only.</span></span> <span data-ttu-id="4e247-115">介面必須有 [**uuid**](uuid.md) 或 [**區域**](local.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4e247-115">An interface must have either a [**uuid**](uuid.md) or a [**local**](local.md) attribute.</span></span>                                                                                             |
| [<span data-ttu-id="4e247-116">**ms 聯 \_ 集**</span><span class="sxs-lookup"><span data-stu-id="4e247-116">**ms\_union**</span></span>](-ms-union.md)              | <span data-ttu-id="4e247-117">控制 nonencapsulated 聯集的 NDR 對齊。</span><span class="sxs-lookup"><span data-stu-id="4e247-117">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="4e247-118">用於回溯相容性與以 MIDL 1.0 或2.0 為基礎的介面。</span><span class="sxs-lookup"><span data-stu-id="4e247-118">Use for backward compatibility with interfaces built on MIDL 1.0 or 2.0.</span></span>                                                                                                                   |
| [<span data-ttu-id="4e247-119">**物件**</span><span class="sxs-lookup"><span data-stu-id="4e247-119">**object**</span></span>](object.md)                    | <span data-ttu-id="4e247-120">將介面識別為 COM 介面，並指示 MIDL 編譯器產生 proxy/stub 程式碼，而不是 RPC 用戶端和伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="4e247-120">Identifies the interface as a COM interface and directs the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span>                                                                                                    |
| [<span data-ttu-id="4e247-121">**版本**</span><span class="sxs-lookup"><span data-stu-id="4e247-121">**version**</span></span>](version.md)                  | <span data-ttu-id="4e247-122">識別介面的多個版本存在時的特定版本。</span><span class="sxs-lookup"><span data-stu-id="4e247-122">Identifies a particular version of an interface in cases where multiple versions of the interface exist.</span></span> <span data-ttu-id="4e247-123">因為 COM 介面是不可變的，所以您無法在 [**物件**](object.md)介面上使用 [**version**](version.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="4e247-123">Because COM interfaces are immutable, you cannot use the [**version**](version.md) attribute on an [**object**](object.md) interface.</span></span> |
| [<span data-ttu-id="4e247-124">**指標 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="4e247-124">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="4e247-125">指定所有指標的預設指標類型，但參數清單中包含的指標除外。</span><span class="sxs-lookup"><span data-stu-id="4e247-125">Specifies the default pointer type for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="4e247-126">預設類型可以是 [**unique**](unique.md)、 [**ref**](ref.md)或 [**ptr**](ptr.md)。</span><span class="sxs-lookup"><span data-stu-id="4e247-126">The default type can be [**unique**](unique.md), [**ref**](ref.md), or [**ptr**](ptr.md).</span></span>                                                   |
| [<span data-ttu-id="4e247-127">**端點**</span><span class="sxs-lookup"><span data-stu-id="4e247-127">**endpoint**</span></span>](endpoint.md)                | <span data-ttu-id="4e247-128">指定伺服器應用程式將接聽遠端程序呼叫的靜態 (已知) 端點。</span><span class="sxs-lookup"><span data-stu-id="4e247-128">Specifies a static (well-known) endpoint on which a server application will listen for remote procedure calls.</span></span>                                                                                                                                   |



 

<span data-ttu-id="4e247-129">請參閱程式庫語句內所定義或參考之介面屬性的 [類型程式庫屬性](type-library-attributes.md) （例如 [**雙重**](dual.md) 和 [**oleautomation**](oleautomation.md)）。</span><span class="sxs-lookup"><span data-stu-id="4e247-129">See [Type Library Attributes](type-library-attributes.md) for interface attributes, such as [**dual**](dual.md) and [**oleautomation**](oleautomation.md), that are specific to interfaces defined or referenced inside a library statement.</span></span>

 

 




