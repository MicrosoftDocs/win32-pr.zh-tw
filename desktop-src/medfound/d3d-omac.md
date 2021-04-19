---
description: 包含訊息驗證碼 (MAC) 。
ms.assetid: be5515fd-1936-46b8-9fc8-8d1f87048c38
title: 'D3D_OMAC 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D_OMAC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21c710b21c31147f7208ddd1637426aeafb60234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971984"
---
# <a name="d3d_omac-structure"></a><span data-ttu-id="fd330-103">D3D \_ OMAC 結構</span><span class="sxs-lookup"><span data-stu-id="fd330-103">D3D\_OMAC structure</span></span>

<span data-ttu-id="fd330-104">包含訊息驗證碼 (MAC) 。</span><span class="sxs-lookup"><span data-stu-id="fd330-104">Contains a Message Authentication Code (MAC).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd330-105">語法</span><span class="sxs-lookup"><span data-stu-id="fd330-105">Syntax</span></span>


```C++
typedef struct _D3D_OMAC {
  BYTE Omac[D3D_OMAC_SIZE];
} D3D_OMAC;
```



## <a name="members"></a><span data-ttu-id="fd330-106">成員</span><span class="sxs-lookup"><span data-stu-id="fd330-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd330-107">**Omac**</span><span class="sxs-lookup"><span data-stu-id="fd330-107">**Omac**</span></span>
</dt> <dd>

<span data-ttu-id="fd330-108">位元組陣列，其中包含訊息的密碼編譯 MAC 值。</span><span class="sxs-lookup"><span data-stu-id="fd330-108">A byte array that contains the cryptographic MAC value of the message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd330-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd330-109">Requirements</span></span>



| <span data-ttu-id="fd330-110">需求</span><span class="sxs-lookup"><span data-stu-id="fd330-110">Requirement</span></span> | <span data-ttu-id="fd330-111">值</span><span class="sxs-lookup"><span data-stu-id="fd330-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd330-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd330-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fd330-113">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd330-113">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fd330-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd330-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fd330-115">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd330-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fd330-116">標頭</span><span class="sxs-lookup"><span data-stu-id="fd330-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd330-117"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd330-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd330-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd330-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd330-119">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="fd330-119">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




