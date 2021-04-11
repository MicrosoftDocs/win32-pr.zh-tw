---
title: 介面金鑰
description: 藉由將介面名稱與介面識別碼 (IID) 產生關聯，以註冊新的介面。 每個新介面都必須有一個 IID 子機碼。
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- 介面登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021807"
---
# <a name="interface-key"></a><span data-ttu-id="88728-105">介面金鑰</span><span class="sxs-lookup"><span data-stu-id="88728-105">Interface Key</span></span>

<span data-ttu-id="88728-106">藉由將介面名稱與介面識別碼 (IID) 產生關聯，以註冊新的介面。</span><span class="sxs-lookup"><span data-stu-id="88728-106">Registers new interfaces by associating an interface name with an interface ID (IID).</span></span> <span data-ttu-id="88728-107">每個新介面都必須有一個 IID 子機碼。</span><span class="sxs-lookup"><span data-stu-id="88728-107">There must be one IID subkey for each new interface.</span></span>

## <a name="registry-key"></a><span data-ttu-id="88728-108">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="88728-108">Registry Key</span></span>

<span data-ttu-id="88728-109">**HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別 \\ 介面** \\ *{* IID *}*</span><span class="sxs-lookup"><span data-stu-id="88728-109">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Interface**\\ *{* IID *}*</span></span>



| <span data-ttu-id="88728-110">登錄值</span><span class="sxs-lookup"><span data-stu-id="88728-110">Registry value</span></span>                               | <span data-ttu-id="88728-111">Description</span><span class="sxs-lookup"><span data-stu-id="88728-111">Description</span></span>                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88728-112">**Typeinterface**</span><span class="sxs-lookup"><span data-stu-id="88728-112">**BaseInterface**</span></span>](baseinterface.md)       | <span data-ttu-id="88728-113">識別目前的介面衍生來源的介面。</span><span class="sxs-lookup"><span data-stu-id="88728-113">Identifies the interface from which the current interface is derived.</span></span>                                  |
| [<span data-ttu-id="88728-114">**NumMethods**</span><span class="sxs-lookup"><span data-stu-id="88728-114">**NumMethods**</span></span>](nummethods.md)             | <span data-ttu-id="88728-115">包含相關聯介面中的方法數目，包括衍生介面的方法。</span><span class="sxs-lookup"><span data-stu-id="88728-115">Contains the number of methods in the associated interface, including methods from derived interfaces.</span></span> |
| [<span data-ttu-id="88728-116">**ProxyStubClsid**</span><span class="sxs-lookup"><span data-stu-id="88728-116">**ProxyStubClsid**</span></span>](proxystubclsid.md)     | <span data-ttu-id="88728-117">將 IID 對應至16位 proxy Dll 中的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="88728-117">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>                                                           |
| [<span data-ttu-id="88728-118">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="88728-118">**ProxyStubClsid32**</span></span>](proxystubclsid32.md) | <span data-ttu-id="88728-119">將 IID 對應至32位 proxy Dll 中的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="88728-119">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="88728-120">備註</span><span class="sxs-lookup"><span data-stu-id="88728-120">Remarks</span></span>

<span data-ttu-id="88728-121">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。</span><span class="sxs-lookup"><span data-stu-id="88728-121">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88728-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="88728-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88728-123">**介面**</span><span class="sxs-lookup"><span data-stu-id="88728-123">**Interface**</span></span>](interface.md)
</dt> </dl>

 

 




