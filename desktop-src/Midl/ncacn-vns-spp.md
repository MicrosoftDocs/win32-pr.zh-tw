---
title: ncacn_vns_spp 屬性
description: Ncacn \_ vns \_ spp 關鍵字會將 BANYAN Vines spp 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682052"
---
# <a name="ncacn_vns_spp-attribute"></a>ncacn \_ vns \_ spp 屬性

**Ncacn \_ vns \_ spp** 關鍵字會將 Banyan Vines spp 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>參數

<dl> <dt>

*伺服器名稱* 
</dt> <dd>

指定伺服器的 StreetTalk 名稱。 名稱的格式為 item@group @organization 。 專案的長度最多可以有31個字元，且群組和組織最多可以有15個字元。

</dd> <dt>

*埠名稱* 
</dt> <dd>

指定 Banyan Vines SPP 埠。 靜態端點的有效範圍是250–511。

</dd> </dl>

## <a name="remarks"></a>備註

為了在 Windows 2000 上執行的分散式應用程式中使用 **ncacn \_ vns \_ spp** 傳輸通訊協定，必須安裝適當的 Banyan 企業用戶端軟體。 安裝之後，開啟 **主控台**，選擇 [設定] **和 [新增**]，然後選取 [ **\| Banyan 的服務 Banyan \| RPC 服務**]。 支援16位用戶端需要適當的 Vines 軟體。 如需 Banyan 企業用戶端產品和16位 Vines 軟體的詳細資訊，請洽詢 Banyan。

Banyan Vines SPP 傳輸埠字串的語法（如同所有的埠字串），會與 IDL 規格分開定義。 編譯器會執行一些語法檢查，但不保證端點規格是正確的。 某些錯誤可能會在執行時間（而不是在編譯時期）回報。

> [!Note]  
> Windows XP 不支援此通訊協定系列。

 

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**端點**](endpoint.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**\_在 \_ dsp ncacn**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ nsp**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ ipx**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[字串系結](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 