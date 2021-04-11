---
title: 手動 SA
description: " (SA) IPsec 原則案例的手動安全性關聯，可讓呼叫者藉由直接指定 IPsec SAs 來保護任何網路流量，以略過內建的 IPsec 加密模組 (IKE 和 AuthIP) 。"
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161447ff5cfd98878ab4ee0f4b18cbcc3a53643
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933143"
---
# <a name="manual-sa"></a>手動 SA

 (SA) IPsec 原則案例的手動安全性關聯，可讓呼叫者藉由直接指定 IPsec SAs 來保護任何網路流量，以略過內建的 IPsec 加密模組 (IKE 和 AuthIP) 。

可能的手動 SA 案例範例是「新增 IPsec SA 組以保護 IP 位址之間的所有單播資料流量 1.1.1.1 & 2.2.2.2，ICMP 除外，使用 IPsec 傳輸模式。」

> [!Note]  
> 您必須在具有適當設定 IP 位址的兩部電腦上執行下列步驟。

 

若要以程式設計方式執行此範例，請使用下列 WFP 設定。

<dl>

**在 FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6} 設定輸入每個封包篩選規則**  

1.  新增具有下列屬性的篩選準則。 
    | 篩選屬性                                                   | 值                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則 | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **FWPM \_ 條件 \_ IP \_ 本機 \_ 位址**                           | 適當的本機位址 (1.1.1.1 或 2.2.2.2) 。           |
    | **FWPM \_ 條件 \_ IP \_ 遠端 \_ 位址**                          | 適當的遠端位址 (1.1.1.1 或 2.2.2.2) 。          |
    | **動作。類型**                                                   | **已 \_ 終止的 .FWP 動作 \_ 標注 \_**                         |
    | **calloutKey**                                             | **FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 傳輸 \_ V {4 \| 6}**         |

        
2.  藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。 
    | 篩選屬性                                                   | 值                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則 | NlatUnicast                                                                |
    | **FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則             | **IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。<br/> |
    | **動作。類型**                                                   | **已 \_ 允許的 .FWP 動作 \_**                                                    |
    | **weight**                                                        | [**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**](filter-weight-identifiers.md)  |

        

**在 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6} 上，設定每個封包篩選規則的輸出**  

1.  新增具有下列屬性的篩選準則。 
    | 篩選屬性                                                   | 值                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | **FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則 | NlatUnicast                                            |
    | **FWPM \_條件 \_ IP \_ 本機 \_ 位址** 篩選準則       | 適當的本機位址 (1.1.1.1 或 2.2.2.2) 。    |
    | **FWPM \_條件 \_ IP \_ 遠端 \_ 位址** 篩選準則      | 適當的遠端位址 (1.1.1.1 或 2.2.2.2) 。   |
    | **動作。類型**                                                   | **已 \_ 終止的 .FWP 動作 \_ 標注 \_**                  |
    | **calloutKey**                                             | **FWPM \_ 標注 \_ IPSEC \_ 輸出 \_ 傳輸 \_ V {4 \| 6}** |

        
2.  藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。 
    | 篩選屬性                                                   | 值                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則 | NlatUnicast                                                                |
    | **FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則             | **IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。<br/> |
    | **動作。類型**                                                   | **已 \_ 允許的 .FWP 動作 \_**                                                    |
    | **weight**                                                        | **FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**                                   |

        

**設定輸入和輸出安全性關聯**

1.  使用 *outboundTraffic* 參數（其中包含作為 1.1.1.1 & 2.2.2.2 的 IP 位址）來呼叫 [**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)，並將 **ipsecFilterId** 作為上面新增的輸出傳輸層 IPsec 標注篩選器的 LUID。
2.  使用 *id* 參數（其中包含從 [**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)傳回的內容識別碼）和 *getSpi* 參數（包含 IPsecSaCoNtextGetSpi0 的 IP 位址）來呼叫 [](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)，並以 1.1.1.1 & 2.2.2.2）和 **ipsecFilterId** 作為上述新增的輸入傳輸層 IPsec 標注篩選器的 LUID。 傳回的 SPI 值是用來做為本機電腦的輸入 SA SPI，以及對應遠端電腦的輸出 SA SPI。 這兩部電腦都必須使用頻外的方式來交換 SPI 值。
3.  使用 *識別碼* 參數（其中包含從 [**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)傳回的內容識別碼）和 *inboundBundle* 參數（描述輸入 SA 的 (，例如輸入 sa SPI、轉換類型、演算法類型、金鑰) 等）來呼叫 [**IPsecSaCoNtextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)。
4.  使用 *識別碼* 參數（其中包含從 [**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)傳回的內容識別碼）和 *outboundBundle* 參數（描述輸出 SA 的 (，例如輸出 sa SPI、轉換類型、演算法類型、金鑰) 等）來呼叫 [**IPsecSaCoNtextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)。

  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[範例程式碼：手動 SA 加密](manual-sa-keying.md)
</dt> <dt>

[**內建的標注識別碼**](built-in-callout-identifiers.md)
</dt> <dt>

[**篩選層識別碼**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

