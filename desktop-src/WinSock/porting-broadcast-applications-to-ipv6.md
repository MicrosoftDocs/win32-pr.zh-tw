---
description: 本節說明將 IPv6 廣播應用程式移植至 Windows 通訊端所提供的多播功能的最佳作法。
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: 將廣播應用程式移植至 IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb54fec87be2aa6174de603d2c3e4d0e640156902002b1e87fab149a70e3d1ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641698"
---
# <a name="porting-broadcast-applications-to-ipv6"></a>將廣播應用程式移植至 IPv6

本節說明將 IPv6 廣播應用程式移植至 Windows 通訊端所提供的多播功能的最佳作法。

## <a name="comparing-ipv4-to-ipv6"></a>比較 IPv4 與 IPv6

準備將 IPv4 廣播應用程式移植到 IPv6 時，最顯著的考慮是： IPv6 沒有任何已實行的廣播概念。 IPv6 會改為使用多播。

IPv6 的多播可以模擬在 IPv4 中找到的傳統廣播功能。 設定 [ipv6 \_ 新增 \_ 成員資格](ipproto-ipv6-socket-options.md) 通訊端選項，將 ipv6 位址設定為連結-本機範圍的所有節點位址 (FF02：： 1) 相當於使用 [ [SO \_ 廣播](socket-options.md) 通訊端] 選項來廣播 IPv4 廣播位址。 此位址有時稱為 *全部節點多播群組*。 針對只想要廣播模擬 IPv6 的應用程式，該方法的運作方式相當。 但是 IPv6 有一個值得注意的差異，就是預設不會收到所有節點多播群組位址上的多播 (預設會收到 IPv4 廣播) 。 應用程式設計人員必須使用 IPV6 \_ 新增 \_ 成員資格通訊端選項，以啟用來自任何來源的多播接收，包括所有節點的多播群組位址。

> [!Note]  
> 在 IPv6 中，會在傳遞至多播通訊端選項或 IOCTL 的引數結構中指定介面選取。

 

但是，針對多部主機提供更豐富、更健全、更有彈性且更容易管理的傳輸，應用程式開發人員應該考慮移至多播模型。

## <a name="moving-to-multicast"></a>移至多播

使用多播時，應用程式設計人員可以選擇性地選擇特定的來源/群組配對，以啟用選擇性的接收模型。 多播接聽程式探索 (IPv6 和第3版的網際網路群組管理通訊協定上的 MLD)  (IGMPv3) IPv4 支援多播程式設計。 此外，多播可讓應用程式特別封鎖群組內的 (或解除封鎖) 的寄件者，進一步保護應用程式免于 rogue 的廣播者。 這項功能適用于 IPv4 (需要 IGMPv3) 和 IPv6 (需要 MLDv2) 。

使用多播的應用程式程式設計人員有兩個主要案例：從 IPv4 廣播移植 (或多播) 應用程式傳送至 IPv6，以及建立新的 IPv6 多播應用程式。

若要移植現有的應用程式，有兩個選項可移至 IPv6 多播：使用通訊端選項和使用 IOCTLs。

-   使用通訊端選項是以變更為基礎的方法，可讓開發人員視需要變更通訊端屬性 (例如封鎖或解除封鎖寄件者、新增來源等) 。 這種方法比較直覺，也是建議的方法。 如需以變更為基礎的多播方法的詳細資訊，請參閱[使用 Windows 通訊端的 MLD 和 IGMP](igmp-and-windows-sockets.md)。
-   使用 IOCTLs 是以最終狀態為基礎的方法，因為它可讓開發人員提供完整設定的通訊端狀態，包括包含和排除清單，以及一個呼叫。 如需以最終狀態為基礎之方法的詳細資訊，請參閱 [最終狀態式多播程式設計](final-state-based-multicast-programming.md)。

針對建立新 IPv6 多播應用程式的應用程式，建議的作法是使用通訊端選項，而不是使用 IOCTLs。

另一種方法是使用 IPv6 來建立多播應用程式，而這需要使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 功能。 雖然不建議使用 **WSAJoinLeaf** 函式，但在某些情況下可能會用到它。 例如，在 Windows Server 2003 及更早版本上使用通訊端選項的一項缺點，就是它們是 IP 版本特定的。 在這些舊版的 Windows 上，IPv6 和 IPv4 的不同通訊端選項必須是。 在 Windows Vista 和更新版本中，支援的新通訊端選項可同時搭配 IPv4 和 IPv6 使用。 相反地， **WSAJoinLeaf** 函式是與 IP 版本和通訊協定無關，因此在建立必須在 Windows Server 2003 及更早版本上使用多個 IP 版本的應用程式時，這是很有用的方法。 在需要通訊協定和 IP 版本 agnosticism 的特定情況下，使用 **WSAJoinLeaf** 函數可能更適合。

 

 



