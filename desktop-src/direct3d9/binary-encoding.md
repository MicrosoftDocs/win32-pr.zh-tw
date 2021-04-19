---
description: 本節詳細說明 directx 3.0 版本所引進的 DirectX (. x) 檔案格式二進位版本。
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: 二進位編碼方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979712"
---
# <a name="binary-encoding"></a><span data-ttu-id="1a6a7-103">二進位編碼方式</span><span class="sxs-lookup"><span data-stu-id="1a6a7-103">Binary Encoding</span></span>

<span data-ttu-id="1a6a7-104">本節詳細說明 directx 3.0 版本所引進的 DirectX (. x) 檔案格式二進位版本。</span><span class="sxs-lookup"><span data-stu-id="1a6a7-104">This section details the binary version of the DirectX (.x) file format as introduced with the release of DirectX 3.0.</span></span>

<span data-ttu-id="1a6a7-105">二進位格式是文字格式的 token 化標記法。</span><span class="sxs-lookup"><span data-stu-id="1a6a7-105">The binary format is a tokenized representation of the text format.</span></span> <span data-ttu-id="1a6a7-106">權杖可以是獨立的，也可以伴隨基本資料記錄。</span><span class="sxs-lookup"><span data-stu-id="1a6a7-106">Tokens can be stand-alone or accompanied by primitive data records.</span></span> <span data-ttu-id="1a6a7-107">獨立權杖會提供語法結構，而且記錄面向權杖會提供必要的資料。</span><span class="sxs-lookup"><span data-stu-id="1a6a7-107">Stand-alone tokens give grammatical structure, and record-bearing tokens supply the necessary data.</span></span>

<span data-ttu-id="1a6a7-108">請注意，所有資料都是以位元組由小到大的格式儲存。</span><span class="sxs-lookup"><span data-stu-id="1a6a7-108">Note that all data is stored in little-endian format.</span></span> <span data-ttu-id="1a6a7-109">有效的二進位資料流程是由標頭後面接著範本和/或資料物件所組成。</span><span class="sxs-lookup"><span data-stu-id="1a6a7-109">A valid binary data stream consists of a header followed by templates and/or data objects.</span></span>

<span data-ttu-id="1a6a7-110">本節將討論二進位檔案格式的下列元件，並提供範例範本和二進位資料物件。</span><span class="sxs-lookup"><span data-stu-id="1a6a7-110">This section discusses the following components of the binary file format and provides an example template and binary data object.</span></span>

-   [<span data-ttu-id="1a6a7-111">標頭</span><span class="sxs-lookup"><span data-stu-id="1a6a7-111">Header</span></span>](header.md)
-   [<span data-ttu-id="1a6a7-112">權杖</span><span class="sxs-lookup"><span data-stu-id="1a6a7-112">Tokens</span></span>](tokens.md)
-   [<span data-ttu-id="1a6a7-113">權杖記錄</span><span class="sxs-lookup"><span data-stu-id="1a6a7-113">Token Records</span></span>](token-records.md)
-   [<span data-ttu-id="1a6a7-114">範本</span><span class="sxs-lookup"><span data-stu-id="1a6a7-114">Templates</span></span>](dx9-graphics-reference-x-file-binaryencoding-templates.md)
-   [<span data-ttu-id="1a6a7-115">資料</span><span class="sxs-lookup"><span data-stu-id="1a6a7-115">Data</span></span>](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [<span data-ttu-id="1a6a7-116">範例</span><span class="sxs-lookup"><span data-stu-id="1a6a7-116">Examples</span></span>](examples.md)

## <a name="related-topics"></a><span data-ttu-id="1a6a7-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a6a7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a6a7-118">X 檔案格式參考</span><span class="sxs-lookup"><span data-stu-id="1a6a7-118">X File Format Reference</span></span>](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



