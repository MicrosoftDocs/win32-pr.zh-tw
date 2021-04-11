---
description: 包含 D3DAUTHENTICATEDCONFIGURE 保護命令的輸入資料 \_ 。
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fc1daee7bfd9320539a03974ab431c4ba588d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847636"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a><span data-ttu-id="2f203-103">D3DAUTHENTICATEDCHANNEL \_ CONFIGUREPROTECTION 結構</span><span class="sxs-lookup"><span data-stu-id="2f203-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREPROTECTION structure</span></span>

<span data-ttu-id="2f203-104">包含 [**D3DAUTHENTICATEDCONFIGURE \_ 保護**](d3dauthenticatedconfigure-protection.md) 命令的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="2f203-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_PROTECTION**](d3dauthenticatedconfigure-protection.md) command.</span></span>

<span data-ttu-id="2f203-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)。</span><span class="sxs-lookup"><span data-stu-id="2f203-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f203-106">語法</span><span class="sxs-lookup"><span data-stu-id="2f203-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a><span data-ttu-id="2f203-107">成員</span><span class="sxs-lookup"><span data-stu-id="2f203-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2f203-108">**參數**</span><span class="sxs-lookup"><span data-stu-id="2f203-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="2f203-109">D3DAUTHENTICATEDCHANNEL 設定包含命令 GUID 和其他資料的 [**\_ \_ 輸入**](d3dauthenticatedchannel-configure-input.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="2f203-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="2f203-110">**保護**</span><span class="sxs-lookup"><span data-stu-id="2f203-110">**Protections**</span></span>
</dt> <dd>

<span data-ttu-id="2f203-111">[**D3DAUTHENTICATEDCHANNEL \_ 保護 \_ 旗標**](d3dauthenticatedchannel-protection-flags.md)結構，可指定保護層級。</span><span class="sxs-lookup"><span data-stu-id="2f203-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f203-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f203-112">Requirements</span></span>



| <span data-ttu-id="2f203-113">需求</span><span class="sxs-lookup"><span data-stu-id="2f203-113">Requirement</span></span> | <span data-ttu-id="2f203-114">值</span><span class="sxs-lookup"><span data-stu-id="2f203-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f203-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f203-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2f203-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f203-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2f203-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f203-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2f203-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f203-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2f203-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2f203-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f203-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f203-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f203-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f203-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f203-122">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="2f203-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="2f203-123">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="2f203-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




