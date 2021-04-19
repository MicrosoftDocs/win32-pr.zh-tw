---
title: WMFILECAPABILITIES 結構
description: WMFILECAPABILITIES 結構描述 MIME 型別。
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- WMFILECAPABILITIES 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975955"
---
# <a name="wmfilecapabilities-structure"></a><span data-ttu-id="9574e-104">WMFILECAPABILITIES 結構</span><span class="sxs-lookup"><span data-stu-id="9574e-104">WMFILECAPABILITIES structure</span></span>

<span data-ttu-id="9574e-105">**WMFILECAPABILITIES** 結構描述 MIME 型別。</span><span class="sxs-lookup"><span data-stu-id="9574e-105">The **WMFILECAPABILITIES** structure describes the MIME type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9574e-106">語法</span><span class="sxs-lookup"><span data-stu-id="9574e-106">Syntax</span></span>


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a><span data-ttu-id="9574e-107">成員</span><span class="sxs-lookup"><span data-stu-id="9574e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9574e-108">**pwszMimeType**</span><span class="sxs-lookup"><span data-stu-id="9574e-108">**pwszMimeType**</span></span>
</dt> <dd>

<span data-ttu-id="9574e-109">MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="9574e-109">MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="9574e-110">**>dwreserved**</span><span class="sxs-lookup"><span data-stu-id="9574e-110">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="9574e-111">**DWORD** 保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="9574e-111">**DWORD** reserved for future use.</span></span> <span data-ttu-id="9574e-112">設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="9574e-112">Set to zero (0).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9574e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9574e-113">Requirements</span></span>



| <span data-ttu-id="9574e-114">需求</span><span class="sxs-lookup"><span data-stu-id="9574e-114">Requirement</span></span> | <span data-ttu-id="9574e-115">值</span><span class="sxs-lookup"><span data-stu-id="9574e-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9574e-116">標頭</span><span class="sxs-lookup"><span data-stu-id="9574e-116">Header</span></span><br/> | <dl> <span data-ttu-id="9574e-117"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9574e-117"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9574e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9574e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9574e-119">**IWMDMDevice2::GetFormatSupport2**</span><span class="sxs-lookup"><span data-stu-id="9574e-119">**IWMDMDevice2::GetFormatSupport2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[<span data-ttu-id="9574e-120">**結構**</span><span class="sxs-lookup"><span data-stu-id="9574e-120">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





