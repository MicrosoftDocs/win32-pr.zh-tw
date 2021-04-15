---
title: Win32_RDSHServer 類別的 GetStringProperty 方法
description: 抓取 Win32 RDSHServer 物件的字串屬性值 \_ 。
ms.assetid: 136cd213-86a6-472a-8853-8d05f992309a
ms.tgt_platform: multiple
keywords:
- GetStringProperty 方法遠端桌面服務
- GetStringProperty 方法遠端桌面服務，Win32_RDSHServer 類別
- Win32_RDSHServer 類別遠端桌面服務，GetStringProperty 方法
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619a034e0a2f89270d21bf0c4fc297b4248cef59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466908"
---
# <a name="getstringproperty-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="1785b-106">Win32 RDSHServer 類別的 GetStringProperty 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1785b-106">GetStringProperty method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="1785b-107">抓取 [**Win32 \_ RDSHServer**](win32-rdshserver.md) 物件的字串屬性值。</span><span class="sxs-lookup"><span data-stu-id="1785b-107">Retrieves a string property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1785b-108">語法</span><span class="sxs-lookup"><span data-stu-id="1785b-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="1785b-109">參數</span><span class="sxs-lookup"><span data-stu-id="1785b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1785b-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1785b-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1785b-111">識別要取得之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1785b-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="1785b-112">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1785b-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1785b-113">接收已抓取的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1785b-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1785b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1785b-114">Return value</span></span>

<span data-ttu-id="1785b-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1785b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1785b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1785b-116">Requirements</span></span>



| <span data-ttu-id="1785b-117">需求</span><span class="sxs-lookup"><span data-stu-id="1785b-117">Requirement</span></span> | <span data-ttu-id="1785b-118">值</span><span class="sxs-lookup"><span data-stu-id="1785b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1785b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1785b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1785b-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="1785b-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1785b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1785b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1785b-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1785b-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1785b-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="1785b-123">Namespace</span></span><br/>                | <span data-ttu-id="1785b-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="1785b-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1785b-125">MOF</span><span class="sxs-lookup"><span data-stu-id="1785b-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1785b-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="1785b-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1785b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1785b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1785b-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1785b-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1785b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1785b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1785b-130">**Win32 \_ RDSHServer**</span><span class="sxs-lookup"><span data-stu-id="1785b-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





