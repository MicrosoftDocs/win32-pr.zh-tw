---
description: EUDCCodeRange 登錄機碼會針對 (字元集) 的各種字碼頁，定義使用者定義的字元 (EUDC) 程式碼範圍。
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975454"
---
# <a name="eudccoderange"></a><span data-ttu-id="59067-103">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="59067-103">EUDCCodeRange</span></span>

<span data-ttu-id="59067-104">EUDCCodeRange 登錄機碼會針對 (字元集) 的各種字碼頁，定義 [使用者定義的字元 (EUDC) ](end-user-defined-characters.md) 程式碼範圍。</span><span class="sxs-lookup"><span data-stu-id="59067-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="59067-105">它僅供建立 EUDCs 的工具使用，而不是對 EUDC 使用者的直接關注。</span><span class="sxs-lookup"><span data-stu-id="59067-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="59067-106">此登錄機碼具有下列登錄位置：</span><span class="sxs-lookup"><span data-stu-id="59067-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="59067-107">HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ 字碼頁 \\ EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="59067-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="59067-108">其格式為：</span><span class="sxs-lookup"><span data-stu-id="59067-108">The format is:</span></span>

<span data-ttu-id="59067-109">EUDCCodeRange 字碼頁 = FromTo \[ 、FromTo\]</span><span class="sxs-lookup"><span data-stu-id="59067-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="59067-110">其中：</span><span class="sxs-lookup"><span data-stu-id="59067-110">where:</span></span>



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59067-111">CodePage</span><span class="sxs-lookup"><span data-stu-id="59067-111">CodePage</span></span> | <span data-ttu-id="59067-112">其中一個字串 "932" (日文) 、"936" (簡體中文) 、"949" (韓文) 、"950" (繁體中文) 或 "Unicode" (Unicode) 。</span><span class="sxs-lookup"><span data-stu-id="59067-112">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="59067-113">不支援其他值。</span><span class="sxs-lookup"><span data-stu-id="59067-113">No other values are supported.</span></span>                                     |
| <span data-ttu-id="59067-114">FromTo</span><span class="sxs-lookup"><span data-stu-id="59067-114">FromTo</span></span>   | <span data-ttu-id="59067-115">由一組4位數的十六進位值所組成的字串值，以連字號 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="59067-115">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="59067-116">最多可以指定四個 FromTo 值，但每個值都必須以逗號分隔， (，) 。</span><span class="sxs-lookup"><span data-stu-id="59067-116">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="59067-117">以下是登錄專案的正確值。</span><span class="sxs-lookup"><span data-stu-id="59067-117">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="59067-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="59067-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59067-119">EUDC 登錄專案</span><span class="sxs-lookup"><span data-stu-id="59067-119">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="59067-120">EUDC</span><span class="sxs-lookup"><span data-stu-id="59067-120">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



