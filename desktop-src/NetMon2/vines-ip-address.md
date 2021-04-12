---
description: VINES \_ ip \_ 位址結構是 VINES 網路上的 ip 位址。
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: 'VINES_IP_ADDRESS 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319495"
---
# <a name="vines_ip_address-structure"></a><span data-ttu-id="97a8c-103">VINES \_ IP \_ 位址結構</span><span class="sxs-lookup"><span data-stu-id="97a8c-103">VINES\_IP\_ADDRESS structure</span></span>

<span data-ttu-id="97a8c-104">**VINES \_ ip \_ 位址** 結構是 VINES 網路上的 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="97a8c-104">The **VINES\_IP\_ADDRESS** structure is an IP address on a Vines network.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a8c-105">語法</span><span class="sxs-lookup"><span data-stu-id="97a8c-105">Syntax</span></span>


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="97a8c-106">成員</span><span class="sxs-lookup"><span data-stu-id="97a8c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="97a8c-107">**NetID**</span><span class="sxs-lookup"><span data-stu-id="97a8c-107">**NetID**</span></span>
</dt> <dd>

<span data-ttu-id="97a8c-108">特定子網上特定電腦的識別碼。</span><span class="sxs-lookup"><span data-stu-id="97a8c-108">The identifier of a specific machine on a specific subnet.</span></span>

</dd> <dt>

<span data-ttu-id="97a8c-109">**SubnetID**</span><span class="sxs-lookup"><span data-stu-id="97a8c-109">**SubnetID**</span></span>
</dt> <dd>

<span data-ttu-id="97a8c-110">整個網路上特定子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="97a8c-110">The identifier of a specific subnet on the whole network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97a8c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="97a8c-111">Requirements</span></span>



| <span data-ttu-id="97a8c-112">需求</span><span class="sxs-lookup"><span data-stu-id="97a8c-112">Requirement</span></span> | <span data-ttu-id="97a8c-113">值</span><span class="sxs-lookup"><span data-stu-id="97a8c-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="97a8c-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97a8c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="97a8c-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97a8c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="97a8c-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97a8c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="97a8c-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97a8c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="97a8c-118">標頭</span><span class="sxs-lookup"><span data-stu-id="97a8c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="97a8c-119"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="97a8c-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




