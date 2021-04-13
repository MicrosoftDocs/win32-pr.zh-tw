---
title: 傳輸模式
description: 傳輸模式 IPsec 原則案例需要所有相符流量的 IPsec 傳輸模式保護。
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb927aff1b3f0e3c7fd13a192f0fcb18fc3ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375140"
---
# <a name="transport-mode"></a>傳輸模式

傳輸模式 IPsec 原則案例需要所有相符流量的 IPsec 傳輸模式保護。 任何相符的純文字流量都會中斷，直到 IKE 或 AuthIP 協商順利完成為止。 如果協商失敗，與對應 IP 位址的連線仍會中斷。

可能的傳輸模式案例的範例是「使用 IPsec 傳輸模式保護所有單播資料流量（ICMP 除外）。」

若要以程式設計方式執行此範例，請使用下列 WFP 設定。

<dl>

**在 FWPM \_ LAYER \_ IKEEXT \_ V {4 \| 6} 安裝程式 MM 的協商原則**  

1.  新增下列一或兩個 MM 原則提供者內容。  
    -   針對 IKE， **FWPM \_ IPSEC \_ IKE \_ MM \_ coNtext** 型別的原則提供者內容。
    -   針對 AuthIP， **FWPM \_ IPSEC \_ AuthIP \_ MM \_ coNtext** 型別的原則提供者內容。

    > [!Note]  
    > 系統將會協商一般的加密模組，並套用對應的 MM 原則。 如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。

     

2.  針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。 
    | 篩選屬性        | 值                                            |
    |------------------------|--------------------------------------------------|
    | 篩選準則   | 空白。 所有流量都會符合篩選。        |
    | **providerCoNtextKey** | 在步驟1中新增的 MM 提供者內容的 GUID。 |

        

**在 FWPM \_ 層 \_ \_ ，IPSEC V {4 \| 6} 安裝 QM 和 EM 協商原則**  

1.  新增下列一或兩個 QM 傳輸模式原則提供者內容。  
    -   針對 IKE， **FWPM \_ IPSEC \_ IKE \_ QM \_ 傳輸 \_ 內容** 類型的原則提供者內容。
    -   針對 AuthIP，FWPM IPSEC AuthIP 型別的原則提供者內容 **\_ \_ \_ QM \_ 傳輸 \_ 內容**。 此內容可以選擇性地包含 AuthIP 擴充模式 (EM) 的協商原則。

    > [!Note]  
    > 系統將會協商一般的加密模組，並套用對應的 QM 原則。 如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。

     

2.  針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。 
    | 篩選屬性        | 值                                            |
    |------------------------|--------------------------------------------------|
    | 篩選準則   | 空白。 所有流量都會符合篩選。        |
    | **providerCoNtextKey** | 在步驟1中新增的 QM 提供者內容的 GUID。 |

        

**在 FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6} 設定輸入每個封包篩選規則**  

1.  新增具有下列屬性的篩選準則。 
    | 篩選屬性                                                   | 值                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則 | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **動作。類型**                                                   | 已 \_ 終止的 .FWP 動作 \_ 標注 \_                             |
    | **calloutKey**                                             | FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 傳輸 \_ V {4 \| 6}             |

        
2.  藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。
    | 篩選屬性                                                  | 值                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | **FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則 | NlatUnicast                                                               |
    | **FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則            | IPPROTO \_ ICMP {V6} 這些常數定義于 winsock2. h 中。<br/>    |
    | **動作。類型**                                                  | 已 \_ 允許的 .FWP 動作 \_                                                       |
    | **weight**                                                       | [**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**](filter-weight-identifiers.md) |

        

**在 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6} 上，設定每個封包篩選規則的輸出**  

1.  新增具有下列屬性的篩選準則。
    | 篩選屬性                                                   | 值                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | **FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則 | NlatUnicast                                        |
    | **動作。類型**                                                   | **已 \_ 終止的 .FWP 動作 \_ 標注 \_**              |
    | **calloutKey**                                             | FWPM \_ 標注 \_ IPSEC \_ 輸出 \_ 傳輸 \_ V {4 \| 6} |

        
2.  藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。
    | 篩選屬性                                                   | 值                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則 | NlatUnicast                                                            |
    | **FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則             | IPPROTO \_ ICMP {V6} 這些常數定義于 winsock2. h 中。<br/> |
    | **動作。類型**                                                   | 已 \_ 允許的 .FWP 動作 \_                                                    |
    | **weight**                                                        | FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免                                   |

        

</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[範例程式碼：使用傳輸模式](using-transport-mode.md)
</dt> <dt>

[**篩選層識別碼**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**提供者內容類型**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[篩選準則](filtering-conditions.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**內建的標注識別碼**](built-in-callout-identifiers.md)
</dt> </dl>

 

