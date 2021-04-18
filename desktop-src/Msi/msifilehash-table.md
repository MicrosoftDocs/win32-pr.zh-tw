---
description: MsiFileHash 資料表是用來儲存 Windows Installer 封裝所提供之原始程式檔的128位雜湊。 雜湊會分割成 4 32 位值，並儲存在資料表的個別資料行中。
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: MsiFileHash 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86acb299e5d7f099a8d49affc64810d128e88369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971382"
---
# <a name="msifilehash-table"></a><span data-ttu-id="b124c-104">MsiFileHash 資料表</span><span class="sxs-lookup"><span data-stu-id="b124c-104">MsiFileHash Table</span></span>

<span data-ttu-id="b124c-105">**MsiFileHash** 資料表是用來儲存 Windows Installer 封裝所提供之原始程式檔的128位雜湊。</span><span class="sxs-lookup"><span data-stu-id="b124c-105">The **MsiFileHash** table is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span> <span data-ttu-id="b124c-106">雜湊會分割成 4 32 位值，並儲存在資料表的個別資料行中。</span><span class="sxs-lookup"><span data-stu-id="b124c-106">The hash is split into four 32-bit values and stored in separate columns of the table.</span></span>

<span data-ttu-id="b124c-107">Windows Installer 可以使用檔案雜湊來偵測和消除不必要的檔案複製。</span><span class="sxs-lookup"><span data-stu-id="b124c-107">Windows Installer can use file hashing as a means to detect and eliminate unnecessary file copying.</span></span> <span data-ttu-id="b124c-108">儲存在 **MsiFileHash** 資料表中的檔案雜湊，可能會與使用者電腦上呼叫 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)所取得的現有檔案雜湊進行比較。</span><span class="sxs-lookup"><span data-stu-id="b124c-108">A file hash stored in the **MsiFileHash** table may be compared to a hash of an existing file on the user's computer obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="b124c-109">**MsiFileHash** 資料表只能搭配未建立版本檔使用。</span><span class="sxs-lookup"><span data-stu-id="b124c-109">The **MsiFileHash** table can only be used with unversioned files.</span></span>

<span data-ttu-id="b124c-110">**MsiFileHash** 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="b124c-110">The **MsiFileHash** table has the following columns.</span></span>



| <span data-ttu-id="b124c-111">Column</span><span class="sxs-lookup"><span data-stu-id="b124c-111">Column</span></span>    | <span data-ttu-id="b124c-112">類型</span><span class="sxs-lookup"><span data-stu-id="b124c-112">Type</span></span>                               | <span data-ttu-id="b124c-113">答案</span><span class="sxs-lookup"><span data-stu-id="b124c-113">Key</span></span> | <span data-ttu-id="b124c-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="b124c-114">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="b124c-115">檔案\_</span><span class="sxs-lookup"><span data-stu-id="b124c-115">File\_</span></span>    | [<span data-ttu-id="b124c-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="b124c-116">Identifier</span></span>](identifier.md)       | <span data-ttu-id="b124c-117">Y</span><span class="sxs-lookup"><span data-stu-id="b124c-117">Y</span></span>   | <span data-ttu-id="b124c-118">N</span><span class="sxs-lookup"><span data-stu-id="b124c-118">N</span></span>        |
| <span data-ttu-id="b124c-119">選項</span><span class="sxs-lookup"><span data-stu-id="b124c-119">Options</span></span>   | [<span data-ttu-id="b124c-120">整數</span><span class="sxs-lookup"><span data-stu-id="b124c-120">Integer</span></span>](integer.md)             | <span data-ttu-id="b124c-121">N</span><span class="sxs-lookup"><span data-stu-id="b124c-121">N</span></span>   | <span data-ttu-id="b124c-122">N</span><span class="sxs-lookup"><span data-stu-id="b124c-122">N</span></span>        |
| <span data-ttu-id="b124c-123">HashPart1</span><span class="sxs-lookup"><span data-stu-id="b124c-123">HashPart1</span></span> | [<span data-ttu-id="b124c-124">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="b124c-124">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="b124c-125">N</span><span class="sxs-lookup"><span data-stu-id="b124c-125">N</span></span>   | <span data-ttu-id="b124c-126">N</span><span class="sxs-lookup"><span data-stu-id="b124c-126">N</span></span>        |
| <span data-ttu-id="b124c-127">HashPart2</span><span class="sxs-lookup"><span data-stu-id="b124c-127">HashPart2</span></span> | [<span data-ttu-id="b124c-128">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="b124c-128">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="b124c-129">N</span><span class="sxs-lookup"><span data-stu-id="b124c-129">N</span></span>   | <span data-ttu-id="b124c-130">N</span><span class="sxs-lookup"><span data-stu-id="b124c-130">N</span></span>        |
| <span data-ttu-id="b124c-131">HashPart3</span><span class="sxs-lookup"><span data-stu-id="b124c-131">HashPart3</span></span> | [<span data-ttu-id="b124c-132">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="b124c-132">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="b124c-133">N</span><span class="sxs-lookup"><span data-stu-id="b124c-133">N</span></span>   | <span data-ttu-id="b124c-134">N</span><span class="sxs-lookup"><span data-stu-id="b124c-134">N</span></span>        |
| <span data-ttu-id="b124c-135">Hashpart4</span><span class="sxs-lookup"><span data-stu-id="b124c-135">Hashpart4</span></span> | [<span data-ttu-id="b124c-136">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="b124c-136">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="b124c-137">N</span><span class="sxs-lookup"><span data-stu-id="b124c-137">N</span></span>   | <span data-ttu-id="b124c-138">N</span><span class="sxs-lookup"><span data-stu-id="b124c-138">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b124c-139">資料行</span><span class="sxs-lookup"><span data-stu-id="b124c-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b124c-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="b124c-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="b124c-141">檔案 [資料表](file-table.md)的外鍵。</span><span class="sxs-lookup"><span data-stu-id="b124c-141">Foreign key to [File table](file-table.md).</span></span> <span data-ttu-id="b124c-142">72字元字串。</span><span class="sxs-lookup"><span data-stu-id="b124c-142">72 char string.</span></span>

</dd> <dt>

<span data-ttu-id="b124c-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>選項</span><span class="sxs-lookup"><span data-stu-id="b124c-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="b124c-144">此資料行必須是0，並保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="b124c-144">This column must be 0 and is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="b124c-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span><span class="sxs-lookup"><span data-stu-id="b124c-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span></span>
</dt> <dd>

<span data-ttu-id="b124c-146">第一個32位的雜湊。</span><span class="sxs-lookup"><span data-stu-id="b124c-146">First 32 bits of hash.</span></span> <span data-ttu-id="b124c-147">您必須藉由呼叫 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 或 [**get-filehash 方法**](installer-filehash.md)來取得此欄位中輸入的檔案雜湊。</span><span class="sxs-lookup"><span data-stu-id="b124c-147">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="b124c-148">請勿使用其他方法。</span><span class="sxs-lookup"><span data-stu-id="b124c-148">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="b124c-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span><span class="sxs-lookup"><span data-stu-id="b124c-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span></span>
</dt> <dd>

<span data-ttu-id="b124c-150">第二個32位的雜湊。</span><span class="sxs-lookup"><span data-stu-id="b124c-150">Second 32 bits of hash.</span></span> <span data-ttu-id="b124c-151">您必須藉由呼叫 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 或 [**get-filehash 方法**](installer-filehash.md)來取得此欄位中輸入的檔案雜湊。</span><span class="sxs-lookup"><span data-stu-id="b124c-151">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="b124c-152">請勿使用其他雜湊方法。</span><span class="sxs-lookup"><span data-stu-id="b124c-152">Do not use other hashing methods.</span></span>

</dd> <dt>

<span data-ttu-id="b124c-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span><span class="sxs-lookup"><span data-stu-id="b124c-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span></span>
</dt> <dd>

<span data-ttu-id="b124c-154">第三個32位的雜湊。</span><span class="sxs-lookup"><span data-stu-id="b124c-154">Third 32 bits of hash.</span></span> <span data-ttu-id="b124c-155">您必須藉由呼叫 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 或 [**get-filehash 方法**](installer-filehash.md)來取得此欄位中輸入的檔案雜湊。</span><span class="sxs-lookup"><span data-stu-id="b124c-155">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="b124c-156">請勿使用其他方法。</span><span class="sxs-lookup"><span data-stu-id="b124c-156">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="b124c-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span><span class="sxs-lookup"><span data-stu-id="b124c-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span></span>
</dt> <dd>

<span data-ttu-id="b124c-158">第四個32位的雜湊。</span><span class="sxs-lookup"><span data-stu-id="b124c-158">Fourth 32 bits of hash.</span></span> <span data-ttu-id="b124c-159">您必須藉由呼叫 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 或 [**get-filehash 方法**](installer-filehash.md)來取得此欄位中輸入的檔案雜湊。</span><span class="sxs-lookup"><span data-stu-id="b124c-159">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="b124c-160">請勿使用其他方法。</span><span class="sxs-lookup"><span data-stu-id="b124c-160">Do not use other methods.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="b124c-161">驗證</span><span class="sxs-lookup"><span data-stu-id="b124c-161">Validation</span></span>

<dl>

[<span data-ttu-id="b124c-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="b124c-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b124c-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="b124c-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b124c-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="b124c-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b124c-165">ICE60</span><span class="sxs-lookup"><span data-stu-id="b124c-165">ICE60</span></span>](ice60.md)  
[<span data-ttu-id="b124c-166">ICE66</span><span class="sxs-lookup"><span data-stu-id="b124c-166">ICE66</span></span>](ice66.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="b124c-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="b124c-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b124c-168">**MsiGetFileHash**</span><span class="sxs-lookup"><span data-stu-id="b124c-168">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[<span data-ttu-id="b124c-169">預設檔案版本控制</span><span class="sxs-lookup"><span data-stu-id="b124c-169">Default File Versioning</span></span>](default-file-versioning.md)
</dt> </dl>

 

 



