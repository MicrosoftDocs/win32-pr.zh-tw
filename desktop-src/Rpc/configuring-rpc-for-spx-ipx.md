---
title: 設定 SPX/IPX 的 RPC
description: 使用 ncacn 的 \_ spx 和 ncadg 的 \_ ipx 傳輸時，伺服器名稱與 Windows 上的伺服器名稱完全相同。
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462340"
---
# <a name="configuring-rpc-for-spxipx"></a>設定 SPX/IPX 的 RPC

使用 ncacn 的 **\_ spx** 和 **ncadg 的 \_ ipx** 傳輸時，伺服器名稱與 Windows 上的伺服器名稱完全相同。 不過，因為名稱是使用 Novell 通訊協定來散發，所以它們必須符合 Novell 命名慣例。 如果伺服器名稱不是有效的 Novell 名稱，伺服器將無法使用 **ncacn 的 \_ spx** 或 **ncadg \_ ipx** 傳輸來建立端點。

有效的 Novell 伺服器名稱只包含0x20 和0x7f 之間的字元。 小寫字元會變更為大寫。 無法使用下列字元：

" \* 、./：; <=>？\[\]\\\|\]

為了維持與第一個 Windows NT 版本的相容性， **ncacn \_ spx** 和 **ncadg \_ ipx** 也可讓您使用伺服器名稱的特殊格式，稱為波狀符號名稱。 波狀符號名稱包含波狀符號 (~) ，後面接著伺服器的八位數網路編號，然後再接著12位數的乙太網路位址。 波形名稱有一個優點，就是它們不需要任何名稱服務功能。 因此，如果您連接到伺服器，則波狀符號名稱將會運作。

下表包含兩個範例設定，說明先前所述的點。



| 元件                            | 設定為      |
|--------------------------------------|--------------------|
| Windows 伺服器                       | NWCS               |
| Windows 用戶端                       | NWCS               |
| 16位 Windows 用戶端，MS-DOS 用戶端 | NetWare 重新導向程式 |



 

上表中的設定要求您的網路上必須有 NetWare 檔案伺服器或路由器。 它會產生最佳效能，因為伺服器名稱會儲存在 NetWare 平構伺服器中。



| 元件                            | 設定為 |
|--------------------------------------|---------------|
| Windows 伺服器                       | SAP 代理程式     |
| Windows 用戶端                       | IPX/SPX       |
| 16位 Windows 用戶端，MS-DOS 用戶端 | IPX/SPX       |



 

第二個設定適用于不包含 NetWare 檔案伺服器或路由器的環境 (例如，兩部電腦的網路： Windows server 和 MS-DOS 用戶端) 。 名稱解析是在第一次呼叫系結控制碼時完成的，會比第一次設定時稍微慢一點。 此外，第二個設定會導致透過網路產生更多流量。

若要執行名稱解析，當 RPC 伺服器使用 SPX 或 IPX 端點時，伺服器名稱和端點會註冊為服務公告通訊協定， (640 類型的 SAP) 伺服器 (十六進位) 。 為了解析伺服器名稱，RPC 用戶端會針對相同類型的所有服務傳送 SAP 要求，然後掃描回應清單中的伺服器名稱。 此進程會在每個系結控制碼的第一個 RPC 呼叫期間發生。 如需有關適用于 Novell 的 SAP 通訊協定的詳細資訊，請參閱您的 NetWare 檔。

> [!Note]  
> 使用 **ncacn \_ spx** 或 **ncadg \_ Ipx** 傳輸的16位 Windows 用戶端應用程式需要安裝 Nwipxspx.dll 的檔案，才能在 WOW 子系統下執行。 請聯絡 Novell 以取得此檔案。

 

 

 




