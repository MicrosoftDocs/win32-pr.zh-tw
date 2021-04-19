---
title: '/metadata_dir 切換 (MIDLRT.EXE 根據) '
description: /Metadata \_ dir 參數指定一或多個包含平臺中繼資料檔案的目錄。
ms.assetid: 578b9d3f-3ee6-4978-9d2a-0c5aee561a30
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
ms.openlocfilehash: 72781641323aa61ae75da256f84f8c1debfd6556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978469"
---
# <a name="metadata_dir-switch-midlrt"></a><span data-ttu-id="923b6-104">/metadata_dir 切換 (MIDLRT.EXE 根據) </span><span class="sxs-lookup"><span data-stu-id="923b6-104">/metadata_dir switch (MIDLRT)</span></span>

<span data-ttu-id="923b6-105">**/Metadata \_ dir** 參數指定一或多個包含平臺中繼資料檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="923b6-105">The **/metadata\_dir** switch specifies one or more directories that contain platform metadata files.</span></span>

``` syntax
midlrt /metadata_dir metadata_directory
```

## <a name="switch-options"></a><span data-ttu-id="923b6-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="923b6-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="923b6-107">*中繼資料 \_ 目錄*</span><span class="sxs-lookup"><span data-stu-id="923b6-107">*metadata\_directory*</span></span> 
</dt> <dd>

<span data-ttu-id="923b6-108">指定包含平臺中繼資料檔案的一或多個目錄。</span><span class="sxs-lookup"><span data-stu-id="923b6-108">Specifies one or more directories that contain platform metadata files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="923b6-109">備註</span><span class="sxs-lookup"><span data-stu-id="923b6-109">Remarks</span></span>

<span data-ttu-id="923b6-110">您可以使用這個參數來指定 Windows 的主要中繼資料檔案的位置，該檔案的名稱為 windows. winmd。</span><span class="sxs-lookup"><span data-stu-id="923b6-110">Use this switch to specify the location of the main metadata file for Windows, which is named windows.winmd.</span></span>

## <a name="examples"></a><span data-ttu-id="923b6-111">範例</span><span class="sxs-lookup"><span data-stu-id="923b6-111">Examples</span></span>

<span data-ttu-id="923b6-112">**midlrt.exe 根據/metadata \_ dir dir1 dir2**</span><span class="sxs-lookup"><span data-stu-id="923b6-112">**midlrt /metadata\_dir dir1 dir2**</span></span>

## <a name="requirements"></a><span data-ttu-id="923b6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="923b6-113">Requirements</span></span>



| <span data-ttu-id="923b6-114">需求</span><span class="sxs-lookup"><span data-stu-id="923b6-114">Requirement</span></span> | <span data-ttu-id="923b6-115">值</span><span class="sxs-lookup"><span data-stu-id="923b6-115">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="923b6-116">用戶端</span><span class="sxs-lookup"><span data-stu-id="923b6-116">Client</span></span><br/> | <span data-ttu-id="923b6-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="923b6-117">Windows 8</span></span><br/>           |
| <span data-ttu-id="923b6-118">伺服器</span><span class="sxs-lookup"><span data-stu-id="923b6-118">Server</span></span><br/> | <span data-ttu-id="923b6-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="923b6-119">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="923b6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="923b6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="923b6-121">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="923b6-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





