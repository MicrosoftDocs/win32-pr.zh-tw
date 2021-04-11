---
title: '遠端存取服務資料類型 (Ras. h) '
description: 遠端存取服務 API 會使用下列資料類型。
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934342"
---
# <a name="remote-access-service-data-types"></a><span data-ttu-id="4ec30-105">遠端存取服務資料類型</span><span class="sxs-lookup"><span data-stu-id="4ec30-105">Remote Access Service Data Types</span></span>

<span data-ttu-id="4ec30-106">遠端存取服務 API 會使用下列資料類型。</span><span class="sxs-lookup"><span data-stu-id="4ec30-106">The following data types are used by the Remote Access Service API.</span></span>


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

<span data-ttu-id="4ec30-107">**RASIPV4ADDR**</span><span class="sxs-lookup"><span data-stu-id="4ec30-107">**RASIPV4ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="4ec30-108">包含 IPv4 位址的 [**in \_ 位址**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) 。</span><span class="sxs-lookup"><span data-stu-id="4ec30-108">A [**in\_addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) that contains an IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="4ec30-109">在 Windows Vista 或更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="4ec30-109">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> <dt>

<span data-ttu-id="4ec30-110">**RASIPV6ADDR**</span><span class="sxs-lookup"><span data-stu-id="4ec30-110">**RASIPV6ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="4ec30-111">包含 IPv6 位址的 [**in6 \_ 位址**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="4ec30-111">A [**in6\_addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) that contains an IPv6 address.</span></span>

> [!Note]  
> <span data-ttu-id="4ec30-112">在 Windows Vista 或更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="4ec30-112">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ec30-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ec30-113">Requirements</span></span>



| <span data-ttu-id="4ec30-114">需求</span><span class="sxs-lookup"><span data-stu-id="4ec30-114">Requirement</span></span> | <span data-ttu-id="4ec30-115">值</span><span class="sxs-lookup"><span data-stu-id="4ec30-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4ec30-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ec30-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec30-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ec30-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4ec30-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ec30-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec30-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ec30-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4ec30-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4ec30-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ec30-121"><dt>Ras。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ec30-121"><dt>Ras.h</dt></span></span> </dl> |



 

