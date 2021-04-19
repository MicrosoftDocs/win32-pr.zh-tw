---
description: 記錄物件的 DataSize 屬性是唯讀屬性，會傳回指定欄位的資料大小。
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Record 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995769"
---
# <a name="recorddatasize-property"></a><span data-ttu-id="4828e-103">Record 屬性</span><span class="sxs-lookup"><span data-stu-id="4828e-103">Record.DataSize property</span></span>

<span data-ttu-id="4828e-104">[**記錄**](record-object.md)物件的 **DataSize** 屬性是唯讀屬性，會傳回指定欄位的資料大小。</span><span class="sxs-lookup"><span data-stu-id="4828e-104">The **DataSize** property of the [**Record**](record-object.md) object is a read-only property that returns the size of the data for the designated field.</span></span> <span data-ttu-id="4828e-105">如果資料是資料流程，則會傳回資料流程長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4828e-105">If the data is a stream, the stream length in bytes is returned.</span></span> <span data-ttu-id="4828e-106">如果資料是字串，則會傳回不含 Null 的字串長度。</span><span class="sxs-lookup"><span data-stu-id="4828e-106">If the data is a string, the string length without Null is returned.</span></span> <span data-ttu-id="4828e-107">如果資料是整數，則會傳回值4， (表示整數) 的大小。</span><span class="sxs-lookup"><span data-stu-id="4828e-107">If the data is an integer, the value 4 is returned (indicating the size of the integer).</span></span> <span data-ttu-id="4828e-108">如果資料為 Null，則會傳回0。</span><span class="sxs-lookup"><span data-stu-id="4828e-108">If the data is Null, 0 is returned.</span></span>

<span data-ttu-id="4828e-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4828e-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4828e-110">語法</span><span class="sxs-lookup"><span data-stu-id="4828e-110">Syntax</span></span>


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a><span data-ttu-id="4828e-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="4828e-111">Property value</span></span>

<span data-ttu-id="4828e-112">記錄中值的必要欄位編號（以1為基礎）。</span><span class="sxs-lookup"><span data-stu-id="4828e-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="4828e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4828e-113">Requirements</span></span>



| <span data-ttu-id="4828e-114">需求</span><span class="sxs-lookup"><span data-stu-id="4828e-114">Requirement</span></span> | <span data-ttu-id="4828e-115">值</span><span class="sxs-lookup"><span data-stu-id="4828e-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4828e-116">版本</span><span class="sxs-lookup"><span data-stu-id="4828e-116">Version</span></span><br/> | <span data-ttu-id="4828e-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4828e-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4828e-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4828e-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4828e-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="4828e-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4828e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4828e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="4828e-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4828e-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4828e-122">IID</span><span class="sxs-lookup"><span data-stu-id="4828e-122">IID</span></span><br/>     | <span data-ttu-id="4828e-123">IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4828e-123">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




