---
description: SIO \_ 位址 \_ 清單 \_ 排序 IOCTL 可讓應用程式開發人員排序 IPv6 和 IPv4 目的地位址的清單，以判斷建立連接的最佳可用位址。 \_ \_ \_ Windows XP 和更新版本支援 SIO 地址清單排序的 IOCTL。
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: 使用 SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0bce27088052bfc029047d5f498ad90962567b50015a5331b26016e455d770
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121140"
---
# <a name="using-sio_address_list_sort"></a>使用 SIO \_ 通訊 \_ 清單 \_ 排序

**SIO \_ 位址 \_ 清單 \_ 排序** IOCTL 可讓應用程式開發人員排序 IPv6 和 IPv4 目的地位址的清單，以判斷建立連接的最佳可用位址。 Windows XP 和更新版本支援 **SIO \_ 位址 \_ 清單 \_ 排序** 的 IOCTL。

在 Windows Vista 和更新版本上， [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)函式會採用提供的潛在 IP 目的地地址清單、將目的地位址與主機電腦的本機 IP 位址配對，並根據最適合兩個對等互連的位址組來排序配對。 在 Windows Vista 和更新版本上，您應該使用 **CreateSortedAddressPairs** 函式，而不是 **SIO \_ 通訊 \_ 清單 \_ 排序** 的 IOCTL。

下列各節說明 **SIO \_ 通訊 \_ 清單 \_ 排序** 的使用考慮。

## <a name="parameters"></a>參數

傳遞至 **SIO \_ 位址 \_ 清單 \_ 排序** 的緩衝區是 [**通訊端 \_ 位址 \_ 清單**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) 結構。 清單中的每個 [**通訊端 \_ 位址**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) 都必須是 SOCKADDR \_ IN6 格式。

**SIO \_ 位址 \_ 清單 \_ 排序** IOCTL 會在 Windows Vista 和更新版本上排序 IPv6 和 IPv4 位址。 清單中要排序的任何 IPv4 位址都必須是 IPv4 對應的 IPv6 位址格式。 如需有關 IPv4 對應 IPv6 位址格式的詳細資訊，請參閱 [雙重堆疊通訊端](dual-stack-sockets.md)。

在 Windows Server 2003 和 Windows XP 上， **SIO \_ 位址 \_ 清單 \_ 排序** 只會排序 IPv6 位址。 不支援 ipv4 對應 IPv6 位址格式的 IPv4 位址。

在輸出中，如果 IOCTL 程式碼判斷某些目的地位址無效，則 [**通訊端 \_ 位址 \_ 清單**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85))結構的 **iAddressCount** 成員可能會小於輸入。

## <a name="sorting-determination"></a>排序決定

SIO 地址清單排序 IOCTL 的 IPv6 位址排序 \_ 順序 \_ 是以前置詞 \_ 原則表格為基礎。 首碼原則表格是使用 *Netsh.exe* 命令列公用程式來設定。 下列命令列程式碼片段說明基本 *Netsh.exe* 首碼原則資料表設定命令：

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> 在 Windows Server 2003 和 Windows XP 上，上面所列的第一個 netsh 命令如下所示。 所有其他相關的命令都相同。

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

位址順序也是由 IETF *(IPv6) 在 Internet Protocol 第6版3484的預設位址選擇* 上所述的演算法所決定。 如需詳細資訊，請參閱 [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484)。  (此資源可能僅提供英文版。 ) 

**SIO \_ 位址 \_ 清單 \_ 排序** 的 IOCTL 會將位址從最差排序到最差，並視需要填滿 **sin6 \_ 範圍 \_ 識別碼** 成員。 針對網站-本機位址，SIO \_ 位址 \_ 清單 \_ 排序會填入範圍識別碼，或移除位址。

**SIO \_ 位址 \_ 清單 \_ 排序** IOCTL 會忽略系結至通訊端的來源位址，而且只會依據作為參數傳遞的目的地地址清單來排序。

在 Windows Vista 和更新版本上，您應該使用 [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)函式，而不是 **SIO \_ 通訊 \_ 清單 \_ 排序** 的 IOCTL。 **CreateSortedAddressPairs** 函式會傳回位址組清單，其中包含本機來源位址和目的地位址。 這會提供應用程式正確的來源位址，以用於每個目的地位址。 應用程式也可以藉由尋找特定的來源位址來篩選結果。 。

## <a name="requirements"></a>規格需求

**SIO \_ 位址 \_ 清單 \_ 排序** IOCTL 定義于 *Winsock2* 標頭檔中。 在 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 發行時，標頭檔的組織已變更，且 **SIO \_ 位址 \_ 清單 \_ 排序** IOCTL 定義于 *Ws2def .h* 標頭檔中。 請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。

Windows XP 和更新版本支援 **SIO \_ 位址 \_ 清單 \_ 排序** 的 IOCTL。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
