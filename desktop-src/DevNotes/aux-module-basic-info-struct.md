---
description: 包含基本的模組資訊。
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: 'AUX_MODULE_BASIC_INFO 結構 (Aux \_ klib .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990727"
---
# <a name="aux_module_basic_info-structure"></a><span data-ttu-id="e609d-103">AUX \_ 模組 \_ 基本 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="e609d-103">AUX\_MODULE\_BASIC\_INFO structure</span></span>

<span data-ttu-id="e609d-104">包含基本的模組資訊。</span><span class="sxs-lookup"><span data-stu-id="e609d-104">Contains basic module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e609d-105">語法</span><span class="sxs-lookup"><span data-stu-id="e609d-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a><span data-ttu-id="e609d-106">成員</span><span class="sxs-lookup"><span data-stu-id="e609d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e609d-107">**Imagebase 設定**</span><span class="sxs-lookup"><span data-stu-id="e609d-107">**ImageBase**</span></span>
</dt> <dd>

<span data-ttu-id="e609d-108">核心位址空間內模組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="e609d-108">The base address of the module within the kernel's address space.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e609d-109">備註</span><span class="sxs-lookup"><span data-stu-id="e609d-109">Remarks</span></span>

<span data-ttu-id="e609d-110">您可以從 [這裡](https://www.microsoft.com/?ref=go)下載可執行此 API 的物件程式庫。</span><span class="sxs-lookup"><span data-stu-id="e609d-110">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="e609d-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e609d-111">Requirements</span></span>



| <span data-ttu-id="e609d-112">需求</span><span class="sxs-lookup"><span data-stu-id="e609d-112">Requirement</span></span> | <span data-ttu-id="e609d-113">值</span><span class="sxs-lookup"><span data-stu-id="e609d-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e609d-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e609d-114">Redistributable</span></span><br/> | <span data-ttu-id="e609d-115">Windows 輔助 API 程式庫1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="e609d-115">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="e609d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="e609d-116">Header</span></span><br/>          | <dl> <span data-ttu-id="e609d-117"><dt>Aux \_ klib。h</dt></span><span class="sxs-lookup"><span data-stu-id="e609d-117"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e609d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e609d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e609d-119">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="e609d-119">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




