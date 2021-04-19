---
title: ncacn_spx 屬性
description: Ncacn \_ spx 關鍵字會將 spx 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967891"
---
# <a name="ncacn_spx-attribute"></a>ncacn \_ spx 屬性

**Ncacn \_ spx** 關鍵字會將 spx 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a>參數

<dl> <dt>

*連結位址* 
</dt> <dd>

指定主機伺服器。 這可以是 (伺服器名稱) 的字元字串，或是包含主機伺服器的網路位址之20位數的十六進位數位 (8 位數) 與節點位址 (12 位數) 串連。 如需如何取得網路位址和節點位址的指示，請參閱備註。 **Null** 字串會指定本機電腦。

</dd> <dt>

*埠名稱* 
</dt> <dd>

指定代表通訊端位址的選用16位數位。 值的範圍可以從1到65535。 未指定任何值時，端點對應服務會選取有效的 *埠名稱* 值。

</dd> </dl>

## <a name="remarks"></a>備註

當您使用 **ncacn 的 \_ spx** 傳輸時，伺服器名稱與32位 Windows 名稱完全相同。 不過，因為名稱是使用 Novell 通訊協定來散發，所以它們必須符合 Novell 命名慣例。 如果伺服器名稱不是有效的 Novell 名稱，伺服器將無法使用 **ncacn 的 \_ spx** 傳輸來建立端點。 以下是 Novell 伺服器名稱禁止的部分字元清單：

" \* + . / : ;< = >？ \[ \] \\ \|

MS 用戶端3.0 提供的 NWLink 版本不支援 **ncacn 的 \_ spx** 傳輸。

使用 **ncacn \_ spx** 傳輸的16位 Windows 用戶端應用程式需要安裝 Nwipxspx.dll 的檔案，才能在 WOW 子系統下執行。 請聯絡 Novell 以取得此檔案。

> [!Note]  
> 若要取得網路和節點位址，請使用 Novell 的 **comcheck** 公用程式或 novell 定義的 API **IPXGetInternetAddress**。 在 Windows 上，您也可以使用 **ipxroute config** 命令取得這些位址。

 

SPX 傳輸埠字串的語法（像是所有的埠字串），會與 IDL 規格分開定義。 編譯器會執行一些語法檢查，但不保證端點規格是正確的。 某些錯誤可能會在執行時間（而不是在編譯時期）回報。

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
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

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[字串系結](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 