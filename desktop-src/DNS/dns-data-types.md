---
title: 'DNS 資料類型 (Windns .h) '
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: 深入瞭解： DNS 資料類型
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2caa113670a749029b70df9772d6e2707684b7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192783"
---
# <a name="dns-data-types"></a><span data-ttu-id="3ce65-104">DNS 資料類型</span><span class="sxs-lookup"><span data-stu-id="3ce65-104">DNS Data Types</span></span>

<span data-ttu-id="3ce65-105">以下是針對 DNS 定義的資料類型：</span><span class="sxs-lookup"><span data-stu-id="3ce65-105">The following data types are defined for DNS:</span></span>


```C++
typedef DWORD IP4_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="3ce65-106">**IP4 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="3ce65-106">**IP4\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="3ce65-107">代表第四版網際網路協定 (IPv4) 位址的值。</span><span class="sxs-lookup"><span data-stu-id="3ce65-107">A value that represents an Internet Protocol version 4 (IPv4) address.</span></span> <span data-ttu-id="3ce65-108">例如，以 **0x7F000001** 的主機位元組順序表示的點十進位 IPv4 位址 **127.0.0.1**。</span><span class="sxs-lookup"><span data-stu-id="3ce65-108">For example, the dotted decimal IPv4 address, **127.0.0.1**, is represented in host byte order as **0x7F000001**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ce65-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ce65-109">Requirements</span></span>



| <span data-ttu-id="3ce65-110">需求</span><span class="sxs-lookup"><span data-stu-id="3ce65-110">Requirement</span></span> | <span data-ttu-id="3ce65-111">值</span><span class="sxs-lookup"><span data-stu-id="3ce65-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce65-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ce65-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce65-113">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ce65-113">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3ce65-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ce65-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce65-115">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ce65-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3ce65-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3ce65-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ce65-117"><dt>Windns。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ce65-117"><dt>Windns.h</dt></span></span> </dl> |



 

 





