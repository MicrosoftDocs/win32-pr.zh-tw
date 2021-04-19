---
title: 'BITS_FILE_PROPERTY_VALUE 結構 (>deliveryoptimization .h) '
description: BITS_FILE_PROPERTY_VALUE 聯集會根據 BITS_FILE_PROPERTY_ID 列舉中的值，提供 DO 檔案的屬性值。
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- BITS_FILE_PROPERTY_VALUE 結構
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 639ea0523c5b92d9764671cb573497223ef968fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966090"
---
# <a name="bits_file_property_value-structure"></a><span data-ttu-id="8f08e-104">BITS_FILE_PROPERTY_VALUE 結構</span><span class="sxs-lookup"><span data-stu-id="8f08e-104">BITS_FILE_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="8f08e-105">**BITS_FILE_PROPERTY_VALUE** 聯集會根據 [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)列舉中的值，提供 DO 檔案的屬性值。</span><span class="sxs-lookup"><span data-stu-id="8f08e-105">The **BITS_FILE_PROPERTY_VALUE** union provides the property value of the DO file based on a value from the [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f08e-106">語法</span><span class="sxs-lookup"><span data-stu-id="8f08e-106">Syntax</span></span>


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="8f08e-107">成員</span><span class="sxs-lookup"><span data-stu-id="8f08e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f08e-108">**String**</span><span class="sxs-lookup"><span data-stu-id="8f08e-108">**String**</span></span>
</dt> <dd>

<span data-ttu-id="8f08e-109">使用屬性識別碼列舉值 **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS** 時，會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="8f08e-109">This value is used when using the property ID enum value **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f08e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f08e-110">Requirements</span></span>



| <span data-ttu-id="8f08e-111">需求</span><span class="sxs-lookup"><span data-stu-id="8f08e-111">Requirement</span></span> | <span data-ttu-id="8f08e-112">值</span><span class="sxs-lookup"><span data-stu-id="8f08e-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f08e-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f08e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8f08e-114">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f08e-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8f08e-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f08e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8f08e-116">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f08e-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8f08e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8f08e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f08e-118"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f08e-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f08e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f08e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f08e-120">**BITS_FILE_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="8f08e-120">**BITS_FILE_PROPERTY_ID**</span></span>](bits-file-property-id-.md)
</dt> <dt>

[<span data-ttu-id="8f08e-121">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="8f08e-121">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[<span data-ttu-id="8f08e-122">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="8f08e-122">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





