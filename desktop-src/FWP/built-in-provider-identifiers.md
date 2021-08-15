---
title: '內建提供者識別碼 (Fwpmu .h) '
description: 內建于 Windows 篩選平台 (WFP) 的提供者識別碼，都是由 GUID 表示。
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8982fe6ebbe3f4cf5135f2b67f07826ddf9d3f970ca0568c7095931c617cdce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951307"
---
# <a name="built-in-provider-identifiers"></a>內建提供者識別碼

內建于 Windows 篩選平台 (WFP) 的提供者識別碼，都是由 GUID 表示。

這些識別碼的定義如下。

<dl> <dt>

<span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**FWPM \_ 提供者 \_ IKEEXT**
</dt> <dd> <dl> <dt>

{10ad9216-ccde-456c-8b16-e9f04e60a90b}
</dt> <dt>



用來識別由 IKE/AuthIP 新增的所有篩選準則。


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**FWPM \_ PROVIDER \_ IPSEC \_ DOS \_ 設定**
</dt> <dd> <dl> <dt>

{3c6c0519-c05c-4bb9-8338-2327814ce8bf}
</dt> <dt>



用來識別 IPsec DoS 保護新增的所有篩選準則。

> [!Note]  
> 僅適用于 Windows 7 和 Windows Server 2008 R2。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**FWPM \_ 提供者 \_ TCP \_ 煙囪 \_ 卸載**
</dt> <dd> <dl> <dt>

{896aa19e-9a34-4bcb-ae79-beb9127c84b9}
</dt> <dt>



用來識別 TCP 煙囪卸載所新增的所有篩選準則。


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**FWPM \_ 提供者 \_ TCP \_ 範本**
</dt> <dd> <dl> <dt>

{76cfcd30-3394-432d-bed3-441ae50e63c3}
</dt> <dt>



用來識別 TCP 範本新增的所有篩選準則。

> [!Note]  
> 僅適用于 Windows 8 和 Windows Server 2012。

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Fwpmu。h</dt> </dl> |



 

 





