---
title: 'INapServerInfo GetNapServerInfo 方法 (NapServerManagement .h) '
description: 抓取 NAP 伺服器的相關資訊。
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- GetNapServerInfo 方法 NAP
- GetNapServerInfo 方法 NAP，INapServerInfo 介面
- INapServerInfo 介面 NAP，GetNapServerInfo 方法
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686620"
---
# <a name="inapserverinfogetnapserverinfo-method"></a><span data-ttu-id="80cd0-106">INapServerInfo：： GetNapServerInfo 方法</span><span class="sxs-lookup"><span data-stu-id="80cd0-106">INapServerInfo::GetNapServerInfo method</span></span>

> [!Note]  
> <span data-ttu-id="80cd0-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="80cd0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="80cd0-108">**INapServerInfo：： GetNapServerInfo** 方法會抓取 NAP 伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80cd0-108">The **INapServerInfo::GetNapServerInfo** method retrieves information about the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="80cd0-109">語法</span><span class="sxs-lookup"><span data-stu-id="80cd0-109">Syntax</span></span>


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="80cd0-110">參數</span><span class="sxs-lookup"><span data-stu-id="80cd0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80cd0-111">*serverName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="80cd0-111">*serverName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80cd0-112">[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="80cd0-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server name.</span></span>

</dd> <dt>

<span data-ttu-id="80cd0-113">*serverDescription* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="80cd0-113">*serverDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80cd0-114">[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含伺服器描述。</span><span class="sxs-lookup"><span data-stu-id="80cd0-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server description.</span></span>

</dd> <dt>

<span data-ttu-id="80cd0-115">*protocolVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="80cd0-115">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80cd0-116">[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="80cd0-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80cd0-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="80cd0-117">Return value</span></span>

<span data-ttu-id="80cd0-118">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="80cd0-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="80cd0-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="80cd0-119">Return code</span></span>                                                                                     | <span data-ttu-id="80cd0-120">Description</span><span class="sxs-lookup"><span data-stu-id="80cd0-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="80cd0-121"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="80cd0-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="80cd0-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="80cd0-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="80cd0-123"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="80cd0-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="80cd0-124">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="80cd0-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="80cd0-125"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="80cd0-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="80cd0-126">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="80cd0-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="80cd0-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="80cd0-127">Requirements</span></span>



| <span data-ttu-id="80cd0-128">需求</span><span class="sxs-lookup"><span data-stu-id="80cd0-128">Requirement</span></span> | <span data-ttu-id="80cd0-129">值</span><span class="sxs-lookup"><span data-stu-id="80cd0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cd0-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80cd0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="80cd0-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="80cd0-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="80cd0-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80cd0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="80cd0-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80cd0-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="80cd0-134">標頭</span><span class="sxs-lookup"><span data-stu-id="80cd0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="80cd0-135"><dt>NapServerManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="80cd0-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="80cd0-136">Idl</span><span class="sxs-lookup"><span data-stu-id="80cd0-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80cd0-137"><dt>NapServerManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="80cd0-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="80cd0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="80cd0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80cd0-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80cd0-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="80cd0-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80cd0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80cd0-141">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="80cd0-141">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> <dt>

[<span data-ttu-id="80cd0-142">**CountedString**</span><span class="sxs-lookup"><span data-stu-id="80cd0-142">**CountedString**</span></span>](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





