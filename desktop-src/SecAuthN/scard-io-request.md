---
description: 捨棄 \_ IO \_ 要求結構會開始通訊協定控制資訊結構。
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: 'SCARD_IO_REQUEST 結構 (Winsmcrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: fe3205311789ee51bb9b96b3b425b735e1fdf887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319104"
---
# <a name="scard_io_request-structure"></a><span data-ttu-id="7a979-103">捨棄 \_ IO \_ 要求結構</span><span class="sxs-lookup"><span data-stu-id="7a979-103">SCARD\_IO\_REQUEST structure</span></span>

<span data-ttu-id="7a979-104">**捨棄 \_ IO \_ 要求** 結構會開始通訊協定控制資訊結構。</span><span class="sxs-lookup"><span data-stu-id="7a979-104">The **SCARD\_IO\_REQUEST** structure begins a protocol control information structure.</span></span> <span data-ttu-id="7a979-105">任何通訊協定特定的資訊，然後緊接在此結構後面。</span><span class="sxs-lookup"><span data-stu-id="7a979-105">Any protocol-specific information then immediately follows this structure.</span></span> <span data-ttu-id="7a979-106">整個結構的長度必須與基礎硬體架構的文字大小一致。</span><span class="sxs-lookup"><span data-stu-id="7a979-106">The entire length of the structure must be aligned with the underlying hardware architecture word size.</span></span> <span data-ttu-id="7a979-107">例如，在 Win32 中，任何 PCI 資訊的長度都必須是四個位元組的倍數，如此才會在32位界限上對齊。</span><span class="sxs-lookup"><span data-stu-id="7a979-107">For example, in Win32 the length of any PCI information must be a multiple of four bytes so that it aligns on a 32-bit boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a979-108">語法</span><span class="sxs-lookup"><span data-stu-id="7a979-108">Syntax</span></span>


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a><span data-ttu-id="7a979-109">成員</span><span class="sxs-lookup"><span data-stu-id="7a979-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a979-110">**dwProtocol**</span><span class="sxs-lookup"><span data-stu-id="7a979-110">**dwProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="7a979-111">使用中的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7a979-111">Protocol in use.</span></span>

</dd> <dt>

<span data-ttu-id="7a979-112">**cbPciLength**</span><span class="sxs-lookup"><span data-stu-id="7a979-112">**cbPciLength**</span></span>
</dt> <dd>

<span data-ttu-id="7a979-113">**捨棄 \_ IO \_ 要求** 結構的長度（以位元組為單位），加上下列任何 PCI 特定資訊。</span><span class="sxs-lookup"><span data-stu-id="7a979-113">Length, in bytes, of the **SCARD\_IO\_REQUEST** structure plus any following PCI-specific information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a979-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a979-114">Requirements</span></span>



| <span data-ttu-id="7a979-115">需求</span><span class="sxs-lookup"><span data-stu-id="7a979-115">Requirement</span></span> | <span data-ttu-id="7a979-116">值</span><span class="sxs-lookup"><span data-stu-id="7a979-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a979-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a979-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7a979-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a979-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7a979-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a979-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7a979-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a979-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a979-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7a979-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a979-122"><dt>Winsmcrd。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a979-122"><dt>Winsmcrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a979-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a979-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a979-124">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="7a979-124">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




