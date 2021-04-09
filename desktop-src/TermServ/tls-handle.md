---
title: TLS_HANDLE
description: 代表遠端桌面授權伺服器的控制碼。
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685711"
---
# <a name="tls_handle"></a><span data-ttu-id="360a1-104">TLS \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="360a1-104">TLS\_HANDLE</span></span>

<span data-ttu-id="360a1-105">代表遠端桌面授權伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="360a1-105">Represents a handle to a Remote Desktop license server.</span></span> <span data-ttu-id="360a1-106">[**TLSConnectToLsServer**](tlsconnecttolsserver.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="360a1-106">This handle is returned by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="360a1-107">此資料類型沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="360a1-107">This data type has no associated header file.</span></span> <span data-ttu-id="360a1-108">若要使用它，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="360a1-108">To use it, you must define it yourself as shown in this topic.</span></span>

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="360a1-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="360a1-109">Requirements</span></span>



| <span data-ttu-id="360a1-110">需求</span><span class="sxs-lookup"><span data-stu-id="360a1-110">Requirement</span></span> | <span data-ttu-id="360a1-111">值</span><span class="sxs-lookup"><span data-stu-id="360a1-111">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="360a1-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="360a1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="360a1-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="360a1-113">Windows Vista</span></span><br/>       |
| <span data-ttu-id="360a1-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="360a1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="360a1-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="360a1-115">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="360a1-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="360a1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="360a1-117">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="360a1-117">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="360a1-118">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="360a1-118">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





