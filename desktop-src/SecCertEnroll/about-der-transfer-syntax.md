---
description: 將編碼規則套用至抽象語法所描述的資料結構會提供傳輸語法，以控制在電腦之間傳送資料流程時，如何組織資料流程中的位元組。
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: DER 傳送語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563028"
---
# <a name="der-transfer-syntax"></a><span data-ttu-id="c3083-103">DER 傳送語法</span><span class="sxs-lookup"><span data-stu-id="c3083-103">DER Transfer Syntax</span></span>

<span data-ttu-id="c3083-104">將編碼規則套用至抽象語法所描述的資料結構會提供傳輸語法，以控制在電腦之間傳送資料流程時，如何組織資料流程中的位元組。</span><span class="sxs-lookup"><span data-stu-id="c3083-104">Applying an encoding rule to the data structures described by an abstract syntax provides a transfer syntax that governs how bytes in a stream are organized when sent between computers.</span></span> <span data-ttu-id="c3083-105">可辨別編碼規則使用的傳輸語法一律遵循 *標記、長度、值* 的格式。</span><span class="sxs-lookup"><span data-stu-id="c3083-105">The transfer syntax used by Distinguished Encoding Rules always follows a *Tag, Length, Value* format.</span></span> <span data-ttu-id="c3083-106">格式通常稱為 TLV 三，其中每個欄位 (T、L 或 V) 包含一或多個位元組。</span><span class="sxs-lookup"><span data-stu-id="c3083-106">The format is usually referred to as a TLV triplet in which each field (T, L, or V) contains one or more bytes.</span></span>

![der 類型、長度和值 (tlv) 三](images/der-tlv-basic.png)

<span data-ttu-id="c3083-108">[ *標記* ] 欄位會指定要傳送的資料結構類型，[ *長度* ] 欄位會指定要傳送之內容的位元組數目，而 [ *值* ] 欄位則包含內容。</span><span class="sxs-lookup"><span data-stu-id="c3083-108">The *Tag* field specifies the type of the data structure being sent, the *Length* field specifies the number of bytes of content being transferred, and the *Value* field contains the content.</span></span> <span data-ttu-id="c3083-109">請注意，如果值欄位包含已建立的資料類型，其 *值* 欄位可以是三個，如下列圖例所示。</span><span class="sxs-lookup"><span data-stu-id="c3083-109">Note that the *Value* field can be a triplet if it contains a constructed data type as shown by the following illustration.</span></span>

![der tlv 三遞迴](images/der-tlv-recursive.png)

<span data-ttu-id="c3083-111">請參閱下列主題，以取得有關 TLV 三個元件的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c3083-111">See the following topics for detailed information about the components of a TLV triplet.</span></span>

-   [<span data-ttu-id="c3083-112">編碼的標記位元組</span><span class="sxs-lookup"><span data-stu-id="c3083-112">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
-   [<span data-ttu-id="c3083-113">編碼的長度和值位元組</span><span class="sxs-lookup"><span data-stu-id="c3083-113">Encoded Length and Value Bytes</span></span>](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a><span data-ttu-id="c3083-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3083-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3083-115">結構化類型</span><span class="sxs-lookup"><span data-stu-id="c3083-115">Constructed Types</span></span>](about-constructed-types.md)
</dt> <dt>

[<span data-ttu-id="c3083-116">可辨別編碼規則</span><span class="sxs-lookup"><span data-stu-id="c3083-116">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 



