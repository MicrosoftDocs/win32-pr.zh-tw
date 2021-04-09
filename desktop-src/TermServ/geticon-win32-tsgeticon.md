---
title: Win32_TSGetIcon 類別的 GetIcon 方法
description: 傳回指定之圖示的內容。
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- GetIcon 方法遠端桌面服務
- GetIcon 方法遠端桌面服務，Win32_TSGetIcon 類別
- Win32_TSGetIcon 類別遠端桌面服務，GetIcon 方法
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934003"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a><span data-ttu-id="53831-106">Win32 TSGetIcon 類別的 GetIcon 方法 \_</span><span class="sxs-lookup"><span data-stu-id="53831-106">GetIcon method of the Win32\_TSGetIcon class</span></span>

<span data-ttu-id="53831-107">傳回指定之圖示的內容。</span><span class="sxs-lookup"><span data-stu-id="53831-107">Returns the contents of the specified icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="53831-108">語法</span><span class="sxs-lookup"><span data-stu-id="53831-108">Syntax</span></span>


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a><span data-ttu-id="53831-109">參數</span><span class="sxs-lookup"><span data-stu-id="53831-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53831-110">*FilePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53831-110">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53831-111">指定檔案的路徑，該檔案包含圖示</span><span class="sxs-lookup"><span data-stu-id="53831-111">Specifies the path to the file that contains the icon</span></span>

</dd> <dt>

<span data-ttu-id="53831-112">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53831-112">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53831-113">指定檔案中的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="53831-113">Specifies the index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="53831-114">*IconContents* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="53831-114">*IconContents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53831-115">成功完成時，會包含圖示的內容。</span><span class="sxs-lookup"><span data-stu-id="53831-115">On successful completion contains the contents of the icon.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53831-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="53831-116">Requirements</span></span>



| <span data-ttu-id="53831-117">需求</span><span class="sxs-lookup"><span data-stu-id="53831-117">Requirement</span></span> | <span data-ttu-id="53831-118">值</span><span class="sxs-lookup"><span data-stu-id="53831-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53831-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53831-119">Minimum supported client</span></span><br/> | <span data-ttu-id="53831-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="53831-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="53831-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53831-121">Minimum supported server</span></span><br/> | <span data-ttu-id="53831-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53831-122">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="53831-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="53831-123">Namespace</span></span><br/>                | <span data-ttu-id="53831-124">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="53831-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="53831-125">MOF</span><span class="sxs-lookup"><span data-stu-id="53831-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53831-126"><dt>TsAllow mof</dt></span><span class="sxs-lookup"><span data-stu-id="53831-126"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="53831-127">DLL</span><span class="sxs-lookup"><span data-stu-id="53831-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53831-128"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53831-128"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53831-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53831-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53831-130">**Win32 \_ TSGetIcon**</span><span class="sxs-lookup"><span data-stu-id="53831-130">**Win32\_TSGetIcon**</span></span>](win32-tsgeticon.md)
</dt> </dl>

 

 





