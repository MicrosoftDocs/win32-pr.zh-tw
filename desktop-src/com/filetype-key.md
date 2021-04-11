---
title: 密碼類型索引鍵
description: GetClassFile 用來比對非複合檔案中各種檔案位元組的模式。
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- 類型登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022014"
---
# <a name="filetype-key"></a><span data-ttu-id="8f9af-104">密碼類型索引鍵</span><span class="sxs-lookup"><span data-stu-id="8f9af-104">FileType Key</span></span>

<span data-ttu-id="8f9af-105">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)用來比對非複合檔案中各種檔案位元組的模式。</span><span class="sxs-lookup"><span data-stu-id="8f9af-105">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8f9af-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="8f9af-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span data-ttu-id="8f9af-107"><span id="offset"></span><span id="OFFSET"></span>*抵消*</span><span class="sxs-lookup"><span data-stu-id="8f9af-107"><span id="offset"></span><span id="OFFSET"></span>*offset*</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-108">決定從檔案的開頭或結尾算起開始比較的距離。</span><span class="sxs-lookup"><span data-stu-id="8f9af-108">Determines how far from the beginning or end of the file to begin the comparison.</span></span> <span data-ttu-id="8f9af-109">如果位移是負值，則比較會從檔案結尾減去位移值開始。</span><span class="sxs-lookup"><span data-stu-id="8f9af-109">If the offset is a negative value, the comparison begins from the end of the file minus the offset value.</span></span> <span data-ttu-id="8f9af-110">除非在前面加上 "0x"，否則 offset 值是十進位類型。</span><span class="sxs-lookup"><span data-stu-id="8f9af-110">The offset value is a decimal type unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-111"><span id="cb"></span><span id="CB"></span>*Cb*</span><span class="sxs-lookup"><span data-stu-id="8f9af-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-112">表示從開始到檔案結尾的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8f9af-112">Represents the length in bytes from the beginning to the end of the file.</span></span> <span data-ttu-id="8f9af-113">代表檔案中的位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="8f9af-113">Represents the byte range in the file.</span></span> <span data-ttu-id="8f9af-114">除非在前面加上 "0x"，否則 *cb* 值是十進位值。</span><span class="sxs-lookup"><span data-stu-id="8f9af-114">The *cb* value is a decimal unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-115"><span id="mask"></span><span id="MASK"></span>*面具*</span><span class="sxs-lookup"><span data-stu-id="8f9af-115"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-116">用於遮罩的二進位值（使用邏輯 AND 運算來執行），以及 *offset* 和 *cb* 指定的位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="8f9af-116">A binary value used for masking, which is performed by using a logical AND operation, and the byte range specified by *offset* and *cb*.</span></span> <span data-ttu-id="8f9af-117">如果省略此值，則會將位元組設定為所有的位元組。</span><span class="sxs-lookup"><span data-stu-id="8f9af-117">If this value is omitted, the bytes are set to all ones.</span></span> <span data-ttu-id="8f9af-118">此值一律為十六進位。</span><span class="sxs-lookup"><span data-stu-id="8f9af-118">This value is always hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-119"><span id="value"></span><span id="VALUE"></span>*價值*</span><span class="sxs-lookup"><span data-stu-id="8f9af-119"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-120">表示必須符合這種檔案類型之檔案的模式。</span><span class="sxs-lookup"><span data-stu-id="8f9af-120">Represents the pattern that must match for a file to be of this file type.</span></span> <span data-ttu-id="8f9af-121">此模式可用來從其內容中正確識別已知的檔案格式，而不是由它的副檔名來識別。</span><span class="sxs-lookup"><span data-stu-id="8f9af-121">The pattern is used to properly identify a known file format from its contents, not by its extension.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f9af-122">備註</span><span class="sxs-lookup"><span data-stu-id="8f9af-122">Remarks</span></span>

<span data-ttu-id="8f9af-123">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)函式會使用專案來比對非複合檔案中不同檔案位元組的模式。</span><span class="sxs-lookup"><span data-stu-id="8f9af-123">Entries are used by the [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) function to match patterns against various file bytes in a non-compound file.</span></span> <span data-ttu-id="8f9af-124">資料 **類型** 有 CLSID 子機碼，其中每個都有一系列的子機碼 **0**、 **1**、 **2**、 **3**。</span><span class="sxs-lookup"><span data-stu-id="8f9af-124">**FileType** has CLSID subkeys, each of which has a series of subkeys **0**, **1**, **2**, **3**.</span></span> <span data-ttu-id="8f9af-125">這些值包含模式，如果相符的話，就會產生指定的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="8f9af-125">These values contain patterns that, if one matches, yield the indicated CLSID.</span></span> <span data-ttu-id="8f9af-126">例如，值為 "0，4，FFFFFFFF，ABCD1234" 表示前4個位元組必須以該順序 ABCD1234。</span><span class="sxs-lookup"><span data-stu-id="8f9af-126">For example, a value of "0, 4, FFFFFFFF, ABCD1234" indicates that the first 4 bytes must be ABCD1234, in that order.</span></span> <span data-ttu-id="8f9af-127">值為 "-4，4，FEFEFEFE" 表示檔案中的最後四個位元組必須是 FEFEFEFE。</span><span class="sxs-lookup"><span data-stu-id="8f9af-127">A value of "-4, 4, FEFEFEFE " indicates that the last four bytes in the file must be FEFEFEFE.</span></span> <span data-ttu-id="8f9af-128">如果其中一種模式相符，則會傳回 CLSID。</span><span class="sxs-lookup"><span data-stu-id="8f9af-128">If either pattern matches, the CLSID is returned.</span></span>

<span data-ttu-id="8f9af-129">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。</span><span class="sxs-lookup"><span data-stu-id="8f9af-129">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f9af-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f9af-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f9af-131">**<\_ 副檔名>**</span><span class="sxs-lookup"><span data-stu-id="8f9af-131">**<file\_extension>**</span></span>](-file-extension--key.md)
</dt> <dt>

[<span data-ttu-id="8f9af-132">**GetClassFile**</span><span class="sxs-lookup"><span data-stu-id="8f9af-132">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




