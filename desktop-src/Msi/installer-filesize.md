---
description: 安裝程式物件的 FileSize 方法會使用 WIN32 API 呼叫來傳回 Path 中指定之檔案的大小。
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: FileSize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986590"
---
# <a name="installerfilesize-method"></a><span data-ttu-id="f710a-103">FileSize 方法</span><span class="sxs-lookup"><span data-stu-id="f710a-103">Installer.FileSize method</span></span>

<span data-ttu-id="f710a-104">[**安裝程式**](installer-object.md)物件的 **FileSize** 方法會使用 WIN32 API 呼叫來傳回 *Path* 中指定之檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="f710a-104">The **FileSize** method of the [**Installer**](installer-object.md) object uses Win32 API calls to return the size of the file specified in *Path*.</span></span>

## <a name="syntax"></a><span data-ttu-id="f710a-105">語法</span><span class="sxs-lookup"><span data-stu-id="f710a-105">Syntax</span></span>


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="f710a-106">參數</span><span class="sxs-lookup"><span data-stu-id="f710a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f710a-107">*路徑*</span><span class="sxs-lookup"><span data-stu-id="f710a-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="f710a-108">必要的字串，其中包含檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="f710a-108">Required string containing the path to the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f710a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f710a-109">Return value</span></span>

<span data-ttu-id="f710a-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f710a-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f710a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f710a-111">Requirements</span></span>



| <span data-ttu-id="f710a-112">需求</span><span class="sxs-lookup"><span data-stu-id="f710a-112">Requirement</span></span> | <span data-ttu-id="f710a-113">值</span><span class="sxs-lookup"><span data-stu-id="f710a-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f710a-114">版本</span><span class="sxs-lookup"><span data-stu-id="f710a-114">Version</span></span><br/> | <span data-ttu-id="f710a-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="f710a-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f710a-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="f710a-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f710a-117">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f710a-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f710a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="f710a-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="f710a-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f710a-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f710a-120">IID</span><span class="sxs-lookup"><span data-stu-id="f710a-120">IID</span></span><br/>     | <span data-ttu-id="f710a-121">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f710a-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




