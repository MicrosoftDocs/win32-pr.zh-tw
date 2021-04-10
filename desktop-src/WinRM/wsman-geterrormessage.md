---
title: 'GetErrorMessage 方法 (WSManDisp .h) '
description: 傳回格式化的字串，其中包含錯誤號碼的文字。
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- GetErrorMessage 方法 Windows 遠端管理
- GetErrorMessage 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，GetErrorMessage 方法
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317255"
---
# <a name="wsmangeterrormessage-method"></a><span data-ttu-id="1a403-106">WSMan. GetErrorMessage 方法</span><span class="sxs-lookup"><span data-stu-id="1a403-106">WSMan.GetErrorMessage method</span></span>

<span data-ttu-id="1a403-107">傳回格式化的字串，其中包含錯誤號碼的文字。</span><span class="sxs-lookup"><span data-stu-id="1a403-107">Returns a formatted string that contains the text of an error number.</span></span> <span data-ttu-id="1a403-108">這個方法會執行與 **Winrm** 命令列 **winrm helpmsg** *decimal 或十六進位錯誤號碼* 相同的操作。</span><span class="sxs-lookup"><span data-stu-id="1a403-108">This method performs the same operation as the **Winrm** command-line **winrm helpmsg** *decimal or hexadecimal error number*.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a403-109">語法</span><span class="sxs-lookup"><span data-stu-id="1a403-109">Syntax</span></span>


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="1a403-110">參數</span><span class="sxs-lookup"><span data-stu-id="1a403-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a403-111">*errorNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1a403-111">*errorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a403-112">來自 WinRM、WinHTTP 或其他作業系統元件之十進位或十六進位的錯誤訊息編號。</span><span class="sxs-lookup"><span data-stu-id="1a403-112">An error message number in decimal or hexadecimal from WinRM, WinHTTP, or other operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="1a403-113">*errorMessage* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1a403-113">*errorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a403-114">格式化為 **Winrm** 命令所傳回之訊息的錯誤訊息字串。</span><span class="sxs-lookup"><span data-stu-id="1a403-114">An error message string formatted like messages returned from the **Winrm** command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a403-115">備註</span><span class="sxs-lookup"><span data-stu-id="1a403-115">Remarks</span></span>

<span data-ttu-id="1a403-116">對應的 c + + 方法是 [**IWSManEx：： GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage)。</span><span class="sxs-lookup"><span data-stu-id="1a403-116">The corresponding C++ method is [**IWSManEx::GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a403-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a403-117">Requirements</span></span>



| <span data-ttu-id="1a403-118">需求</span><span class="sxs-lookup"><span data-stu-id="1a403-118">Requirement</span></span> | <span data-ttu-id="1a403-119">值</span><span class="sxs-lookup"><span data-stu-id="1a403-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a403-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a403-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1a403-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a403-121">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="1a403-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a403-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1a403-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a403-123">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1a403-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1a403-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a403-125"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a403-125"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a403-126">Idl</span><span class="sxs-lookup"><span data-stu-id="1a403-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1a403-127"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a403-127"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="1a403-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="1a403-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a403-129"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1a403-129"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1a403-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1a403-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a403-131"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a403-131"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1a403-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a403-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a403-133">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="1a403-133">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





