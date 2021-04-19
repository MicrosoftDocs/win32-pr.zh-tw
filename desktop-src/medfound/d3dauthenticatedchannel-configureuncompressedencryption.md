---
description: 包含 D3DAUTHENTICATEDCONFIGURE ENCRYPTIONWHENACCESSIBLE 命令的輸入資料 \_ 。
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c8ea4360ff7f2bbcf2c03040671013473e9873a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970354"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a><span data-ttu-id="291fb-103">D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION 結構</span><span class="sxs-lookup"><span data-stu-id="291fb-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION structure</span></span>

<span data-ttu-id="291fb-104">包含 [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) 命令的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="291fb-104">Contains input data for the [**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) command.</span></span>

<span data-ttu-id="291fb-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)。</span><span class="sxs-lookup"><span data-stu-id="291fb-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="291fb-106">語法</span><span class="sxs-lookup"><span data-stu-id="291fb-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  GUID                                    EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION;
```



## <a name="members"></a><span data-ttu-id="291fb-107">成員</span><span class="sxs-lookup"><span data-stu-id="291fb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="291fb-108">**參數**</span><span class="sxs-lookup"><span data-stu-id="291fb-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="291fb-109">D3DAUTHENTICATEDCHANNEL 設定包含命令 GUID 和其他資料的 [**\_ \_ 輸入**](d3dauthenticatedchannel-configure-input.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="291fb-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="291fb-110">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="291fb-110">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="291fb-111">GUID，指定要套用的加密類型。</span><span class="sxs-lookup"><span data-stu-id="291fb-111">A GUID that specifies the type of encryption to apply.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="291fb-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="291fb-112">Requirements</span></span>



| <span data-ttu-id="291fb-113">需求</span><span class="sxs-lookup"><span data-stu-id="291fb-113">Requirement</span></span> | <span data-ttu-id="291fb-114">值</span><span class="sxs-lookup"><span data-stu-id="291fb-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="291fb-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="291fb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="291fb-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="291fb-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="291fb-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="291fb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="291fb-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="291fb-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="291fb-119">標頭</span><span class="sxs-lookup"><span data-stu-id="291fb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="291fb-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="291fb-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="291fb-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="291fb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="291fb-122">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="291fb-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="291fb-123">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="291fb-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




