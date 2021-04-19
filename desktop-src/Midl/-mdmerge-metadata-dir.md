---
title: '/metadata_dir 切換 (MDMERGE) '
description: /Metadata \_ dir 參數指定包含平臺中繼資料檔案的目錄。
ms.assetid: E95D410B-D384-4337-B0A0-6D5DDA3BE699
keywords:
- /metadata_dir switch MIDL
topic_type:
- apiref
api_name:
- /metadata_dir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd104ae63378056babdc804a93564be4005246c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001196"
---
# <a name="metadata_dir-switch-mdmerge"></a><span data-ttu-id="4eb34-104">/metadata_dir 切換 (MDMERGE) </span><span class="sxs-lookup"><span data-stu-id="4eb34-104">/metadata_dir switch (MDMERGE)</span></span>

<span data-ttu-id="4eb34-105">**/Metadata \_ dir** 參數指定包含平臺中繼資料檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="4eb34-105">The **/metadata\_dir** switch specifies the directory that contains platform metadata files.</span></span>

``` syntax
mdmerge /metadata_dir metadata_directory
```

## <a name="switch-options"></a><span data-ttu-id="4eb34-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="4eb34-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="4eb34-107">*中繼資料 \_ 目錄*</span><span class="sxs-lookup"><span data-stu-id="4eb34-107">*metadata\_directory*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb34-108">指定包含平臺中繼資料檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="4eb34-108">Specifies the directory that contains platform metadata files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4eb34-109">備註</span><span class="sxs-lookup"><span data-stu-id="4eb34-109">Remarks</span></span>

<span data-ttu-id="4eb34-110">您可以使用這個參數來指定 Windows 的主要中繼資料檔案的位置，該檔案的名稱為 windows. winmd。</span><span class="sxs-lookup"><span data-stu-id="4eb34-110">Use this switch to specify the location of the main metadata file for Windows, which is named windows.winmd.</span></span>

## <a name="examples"></a><span data-ttu-id="4eb34-111">範例</span><span class="sxs-lookup"><span data-stu-id="4eb34-111">Examples</span></span>

<span data-ttu-id="4eb34-112">**mdmerge/metadata \_ dir dir1**</span><span class="sxs-lookup"><span data-stu-id="4eb34-112">**mdmerge /metadata\_dir dir1**</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb34-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4eb34-113">Requirements</span></span>



| <span data-ttu-id="4eb34-114">需求</span><span class="sxs-lookup"><span data-stu-id="4eb34-114">Requirement</span></span> | <span data-ttu-id="4eb34-115">值</span><span class="sxs-lookup"><span data-stu-id="4eb34-115">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="4eb34-116">用戶端</span><span class="sxs-lookup"><span data-stu-id="4eb34-116">Client</span></span><br/> | <span data-ttu-id="4eb34-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4eb34-117">Windows 8</span></span><br/>           |
| <span data-ttu-id="4eb34-118">伺服器</span><span class="sxs-lookup"><span data-stu-id="4eb34-118">Server</span></span><br/> | <span data-ttu-id="4eb34-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4eb34-119">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4eb34-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4eb34-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb34-121">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="4eb34-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





