---
description: 包含擴充的模組資訊。
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: 'AUX_MODULE_EXTENDED_INFO 結構 (Aux \_ klib .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981389"
---
# <a name="aux_module_extended_info-structure"></a><span data-ttu-id="ce455-103">AUX \_ 模組 \_ 擴充 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="ce455-103">AUX\_MODULE\_EXTENDED\_INFO structure</span></span>

<span data-ttu-id="ce455-104">包含擴充的模組資訊。</span><span class="sxs-lookup"><span data-stu-id="ce455-104">Contains extended module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce455-105">語法</span><span class="sxs-lookup"><span data-stu-id="ce455-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a><span data-ttu-id="ce455-106">成員</span><span class="sxs-lookup"><span data-stu-id="ce455-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce455-107">**BasicInfo**</span><span class="sxs-lookup"><span data-stu-id="ce455-107">**BasicInfo**</span></span>
</dt> <dd>

<span data-ttu-id="ce455-108">[**AUX \_ 模組 \_ 基本 \_ 資訊**](aux-module-basic-info-struct.md)結構。</span><span class="sxs-lookup"><span data-stu-id="ce455-108">An [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce455-109">**ImageSize**</span><span class="sxs-lookup"><span data-stu-id="ce455-109">**ImageSize**</span></span>
</dt> <dd>

<span data-ttu-id="ce455-110">已載入模組的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce455-110">The size, in bytes, of the loaded module.</span></span>

</dd> <dt>

<span data-ttu-id="ce455-111">**FileNameOffset**</span><span class="sxs-lookup"><span data-stu-id="ce455-111">**FileNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="ce455-112">**FullPathName** 緩衝區內檔案名的位移。</span><span class="sxs-lookup"><span data-stu-id="ce455-112">The offset of the file name within the **FullPathName** buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ce455-113">**FullPathName**</span><span class="sxs-lookup"><span data-stu-id="ce455-113">**FullPathName**</span></span>
</dt> <dd>

<span data-ttu-id="ce455-114">模組的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ce455-114">The full path of the module.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce455-115">備註</span><span class="sxs-lookup"><span data-stu-id="ce455-115">Remarks</span></span>

<span data-ttu-id="ce455-116">您可以從 [這裡](https://www.microsoft.com/?ref=go)下載可執行此 API 的物件程式庫。</span><span class="sxs-lookup"><span data-stu-id="ce455-116">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce455-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce455-117">Requirements</span></span>



| <span data-ttu-id="ce455-118">需求</span><span class="sxs-lookup"><span data-stu-id="ce455-118">Requirement</span></span> | <span data-ttu-id="ce455-119">值</span><span class="sxs-lookup"><span data-stu-id="ce455-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce455-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ce455-120">Redistributable</span></span><br/> | <span data-ttu-id="ce455-121">Windows 輔助 API 程式庫1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="ce455-121">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="ce455-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ce455-122">Header</span></span><br/>          | <dl> <span data-ttu-id="ce455-123"><dt>Aux \_ klib。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce455-123"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce455-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce455-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce455-125">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="ce455-125">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[<span data-ttu-id="ce455-126">**AUX \_ 模組 \_ 基本 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ce455-126">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




