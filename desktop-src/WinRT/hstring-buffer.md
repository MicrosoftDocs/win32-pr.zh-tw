---
description: 可變動字串緩衝區的控制碼，可供您用來建立 HSTRING。
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: 'HSTRING_BUFFER (Hstring) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972223"
---
# <a name="hstring_buffer"></a><span data-ttu-id="29bee-103">HSTRING \_ 緩衝區</span><span class="sxs-lookup"><span data-stu-id="29bee-103">HSTRING\_BUFFER</span></span>

<span data-ttu-id="29bee-104">可變動字串緩衝區的控制碼，可供您用來建立 [**HSTRING**](hstring.md)。</span><span class="sxs-lookup"><span data-stu-id="29bee-104">A handle to a mutable string buffer that you can use to create an [**HSTRING**](hstring.md).</span></span>


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a><span data-ttu-id="29bee-105">備註</span><span class="sxs-lookup"><span data-stu-id="29bee-105">Remarks</span></span>

<span data-ttu-id="29bee-106">**HSTRING \_BUFFER** 表示字串緩衝區，您可以在將其轉換為不可變的 [**HSTRING**](hstring.md)之前加以修改。</span><span class="sxs-lookup"><span data-stu-id="29bee-106">**HSTRING\_BUFFER** represents a string buffer that you can modify before converting it to an immutable [**HSTRING**](hstring.md).</span></span>

<span data-ttu-id="29bee-107">呼叫 [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) 函數來建立 **HSTRING \_ 緩衝區**。</span><span class="sxs-lookup"><span data-stu-id="29bee-107">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to create an **HSTRING\_BUFFER**.</span></span> <span data-ttu-id="29bee-108">呼叫 [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) ，將 **HSTRING \_ 緩衝區** 轉換成不可變的 [**HSTRING**](hstring.md)。</span><span class="sxs-lookup"><span data-stu-id="29bee-108">Call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) to convert an **HSTRING\_BUFFER** to an immutable [**HSTRING**](hstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29bee-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="29bee-109">Requirements</span></span>



| <span data-ttu-id="29bee-110">需求</span><span class="sxs-lookup"><span data-stu-id="29bee-110">Requirement</span></span> | <span data-ttu-id="29bee-111">值</span><span class="sxs-lookup"><span data-stu-id="29bee-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="29bee-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29bee-112">Minimum supported client</span></span><br/> | <span data-ttu-id="29bee-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="29bee-113">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="29bee-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29bee-114">Minimum supported server</span></span><br/> | <span data-ttu-id="29bee-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29bee-115">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="29bee-116">標頭</span><span class="sxs-lookup"><span data-stu-id="29bee-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="29bee-117"><dt>Hstring。h</dt></span><span class="sxs-lookup"><span data-stu-id="29bee-117"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29bee-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29bee-118">See also</span></span>

<dl> <span data-ttu-id="29bee-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="29bee-119"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="29bee-120">**HSTRING**</span><span class="sxs-lookup"><span data-stu-id="29bee-120">**HSTRING**</span></span>](hstring.md)
</dt> <dt>

[<span data-ttu-id="29bee-121">**WindowsPreallocateStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="29bee-121">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[<span data-ttu-id="29bee-122">**WindowsPromoteStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="29bee-122">**WindowsPromoteStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
