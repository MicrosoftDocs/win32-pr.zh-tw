---
title: 資料類型屬性
description: 您可以將這些屬性套用至 typedef 語句中的資料類型，以進一步定義資料類型的使用方式或效果。
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- IDL MIDL、屬性、資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675779"
---
# <a name="data-type-attributes"></a><span data-ttu-id="868d6-104">資料類型屬性</span><span class="sxs-lookup"><span data-stu-id="868d6-104">Data Type Attributes</span></span>

<span data-ttu-id="868d6-105">您可以將這些屬性套用至 [**typedef**](typedef.md) 語句中的資料類型，以進一步定義資料類型的使用方式或效果。</span><span class="sxs-lookup"><span data-stu-id="868d6-105">You can apply these attributes to data types in a [**typedef**](typedef.md) statement to further define the usage or effect of the data type.</span></span>



| <span data-ttu-id="868d6-106">屬性</span><span class="sxs-lookup"><span data-stu-id="868d6-106">Attribute</span></span>                                 | <span data-ttu-id="868d6-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="868d6-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="868d6-108">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="868d6-108">**context\_handle**</span></span>](context-handle.md) | <span data-ttu-id="868d6-109">識別系結控制碼，此控制碼會維護特定用戶端遠端程序呼叫之間特定伺服器的狀態 (內容) 資訊。</span><span class="sxs-lookup"><span data-stu-id="868d6-109">Identifies a binding handle that maintains state (context) information on a particular server between remote procedure calls from a particular client.</span></span> <span data-ttu-id="868d6-110">對 [**物件**](object.md) 介面函式無效。</span><span class="sxs-lookup"><span data-stu-id="868d6-110">Not valid for [**object**](object.md) interface functions.</span></span>                                                                                                         |
| [<span data-ttu-id="868d6-111">**處理**</span><span class="sxs-lookup"><span data-stu-id="868d6-111">**handle**</span></span>](handle.md)                  | <span data-ttu-id="868d6-112">指定應用程式特定的自訂控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="868d6-112">Specifies a custom handle type specific to the application.</span></span>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="868d6-113">**ms 聯 \_ 集**</span><span class="sxs-lookup"><span data-stu-id="868d6-113">**ms\_union**</span></span>](-ms-union.md)            | <span data-ttu-id="868d6-114">控制 nonencapsulated 聯集的 NDR 對齊。</span><span class="sxs-lookup"><span data-stu-id="868d6-114">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="868d6-115">在 [**typedef**](typedef.md)上使用，以使用以 MIDL 1.0 或2.0 建立的介面回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="868d6-115">Use on [**typedef**](typedef.md)s for backward compatibility with interfaces built with MIDL 1.0 or 2.0.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="868d6-116">**管道**</span><span class="sxs-lookup"><span data-stu-id="868d6-116">**pipe**</span></span>](pipe.md)                      | <span data-ttu-id="868d6-117">允許在遠端程序呼叫之間傳輸具類型資料的開放式資料流程。</span><span class="sxs-lookup"><span data-stu-id="868d6-117">Allows transmission of an open-ended stream of typed data across a remote procedure call.</span></span> <span data-ttu-id="868d6-118">[**In**](in.md) pipe 參數可讓伺服器在遠端程序呼叫期間，從用戶端提取資料流程。</span><span class="sxs-lookup"><span data-stu-id="868d6-118">An [**in**](in.md) pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="868d6-119">[**輸出**](-out.md)管道參數可讓伺服器將資料流程推送回用戶端。</span><span class="sxs-lookup"><span data-stu-id="868d6-119">An [**out**](-out.md) pipe parameter allows the server to push the data stream back to the client.</span></span> |
| [<span data-ttu-id="868d6-120">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="868d6-120">**transmit\_as**</span></span>](transmit-as.md)       | <span data-ttu-id="868d6-121">指定如何透過網路傳輸資料類型，用於自訂封送處理。</span><span class="sxs-lookup"><span data-stu-id="868d6-121">Specifies how a data type will be transmitted over a network, used for custom marshaling.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="868d6-122">**v1 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="868d6-122">**v1\_enum**</span></span>](v1-enum.md)               | <span data-ttu-id="868d6-123">指示以32位實體（而非16位預設值）傳輸指定的列舉型別。</span><span class="sxs-lookup"><span data-stu-id="868d6-123">Directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>                                                                                                                                                                                                              |
| [<span data-ttu-id="868d6-124">**網路 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="868d6-124">**wire\_marshal**</span></span>](wire-marshal.md)     | <span data-ttu-id="868d6-125">類似于 [**傳送 \_ as**](transmit-as.md) ，但您會執行常式來調整大小、封送處理、unmarshal 和釋放資料。</span><span class="sxs-lookup"><span data-stu-id="868d6-125">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span>                                                                                                                                                                                              |



 

 

 




