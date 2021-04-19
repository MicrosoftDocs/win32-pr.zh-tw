---
title: OPAQUECOMMAND 結構
description: OPAQUECOMMAND 結構包含命令的資料，這些命令是透過 Windows Media 裝置管理員傳遞至裝置，但不適合 Windows Media 裝置管理員。
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- OPAQUECOMMAND 結構 windows Media 裝置管理員
- 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998832"
---
# <a name="opaquecommand-structure"></a><span data-ttu-id="e3842-105">OPAQUECOMMAND 結構</span><span class="sxs-lookup"><span data-stu-id="e3842-105">OPAQUECOMMAND structure</span></span>

<span data-ttu-id="e3842-106">**OPAQUECOMMAND** 結構包含命令的資料，這些命令是透過 windows media 裝置管理員傳遞至裝置，但不適合 Windows media 裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="e3842-106">The **OPAQUECOMMAND** structure contains data for commands that are passed through Windows Media Device Manager to a device but are not intended to be acted upon by Windows Media Device Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3842-107">語法</span><span class="sxs-lookup"><span data-stu-id="e3842-107">Syntax</span></span>


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a><span data-ttu-id="e3842-108">成員</span><span class="sxs-lookup"><span data-stu-id="e3842-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3842-109">**guidCommand**</span><span class="sxs-lookup"><span data-stu-id="e3842-109">**guidCommand**</span></span>
</dt> <dd>

<span data-ttu-id="e3842-110">代表所要求命令的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="e3842-110">**GUID** representing the requested command.</span></span>

</dd> <dt>

<span data-ttu-id="e3842-111">**dwDataLen**</span><span class="sxs-lookup"><span data-stu-id="e3842-111">**dwDataLen**</span></span>
</dt> <dd>

<span data-ttu-id="e3842-112">*.Pdata* 點之資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e3842-112">Length of the data to which *pData* points, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e3842-113">**.Pdata**</span><span class="sxs-lookup"><span data-stu-id="e3842-113">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="e3842-114">執行命令所需的資料，以及（或）命令所傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="e3842-114">Data required to execute the command, and/or data returned by the command.</span></span>

</dd> <dt>

<span data-ttu-id="e3842-115">**abMAC \[ 20\]**</span><span class="sxs-lookup"><span data-stu-id="e3842-115">**abMAC\[20\]**</span></span>
</dt> <dd>

<span data-ttu-id="e3842-116">此訊息驗證程式代碼 (MAC) 應該包含 **guidCommand** 成員、 *pdwDataLen* 所指向的資料，以及 *.pdata* 點的資料（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="e3842-116">This message authentication code (MAC) should include the **guidCommand** member, the data to which *pdwDataLen* points, and the data to which *pData* points, if any.</span></span> <span data-ttu-id="e3842-117">如果 *.pdata* 為 **Null**，則不得包含在 MAC 中。</span><span class="sxs-lookup"><span data-stu-id="e3842-117">If *pData* is **NULL**, it must not be included in the MAC.</span></span> <span data-ttu-id="e3842-118">WMDM \_ MAC \_ 長度定義為20。</span><span class="sxs-lookup"><span data-stu-id="e3842-118">WMDM\_MAC\_LENGTH is defined as 20.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3842-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3842-119">Requirements</span></span>



| <span data-ttu-id="e3842-120">需求</span><span class="sxs-lookup"><span data-stu-id="e3842-120">Requirement</span></span> | <span data-ttu-id="e3842-121">值</span><span class="sxs-lookup"><span data-stu-id="e3842-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e3842-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e3842-122">Header</span></span><br/> | <dl> <span data-ttu-id="e3842-123"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3842-123"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3842-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3842-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3842-125">**IMDSPDevice::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="e3842-125">**IMDSPDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="e3842-126">**IMDSPStorage::SendOpaqueCommands**</span><span class="sxs-lookup"><span data-stu-id="e3842-126">**IMDSPStorage::SendOpaqueCommands**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="e3842-127">**IWMDMDevice::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="e3842-127">**IWMDMDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="e3842-128">**IWMDMStorage::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="e3842-128">**IWMDMStorage::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="e3842-129">**結構**</span><span class="sxs-lookup"><span data-stu-id="e3842-129">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





