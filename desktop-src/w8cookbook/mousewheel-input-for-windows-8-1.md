---
title: Windows 8.1 的滑鼠滾輪輸入
description: Windows 8.1 的滑鼠滾輪輸入
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2285d2a0456376b01289ac7a4c2607117441384ebd13b0aaf0a162eac50fdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211381"
---
# <a name="mousewheel-input-for-windows-81"></a>Windows 8.1 的滑鼠滾輪輸入

## <a name="platform"></a>平台

<dl> 用戶端-Windows 8。1  
伺服器-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

在 Windows 8.1 中，不再以 Windows 的舊版鍵盤焦點為基礎來傳遞滑鼠滾輪事件。 在 Windows 8.1 中，如果滑鼠停留在商店應用程式上，滑鼠滾輪將會傳遞給該應用程式;不過，基於相容性的目的，如果滑鼠停留在桌面應用程式上，則會繼續根據鍵盤焦點來傳遞滑鼠滾輪。

## <a name="manifestations"></a>表現

當滑鼠停留在商店應用程式上時，滑鼠滾輪會在沒有使用者按一下 Store 應用程式的情況下，滾動任何適用的內容。 這也適用于 [開始] 畫面。 這可讓您在 Windows 8.1 中滑鼠滾輪比 Windows 8 更簡單的互動來進行滾動。

## <a name="mitigation"></a>降低

在大部分的情況下，這種變更應該不會影響現有的應用程式。 如果商店應用程式只在註冊滑鼠點按事件之後才接聽滑鼠滾輪事件，該應用程式就不可能回應滑鼠滾輪，直到使用者主動按一下為止。 因此，此處最有可能的缺點是，應用程式會繼續運作，就像在 Windows 8 一樣。 針對桌面應用程式，讓鍵盤焦點不再讓應用程式具有滑鼠滾輪輸入的 monopoly，但這也不會以任何方式中斷這些應用程式。 因此，不需要短期的緩和措施。

## <a name="solution"></a>解決方案

Store 應用程式開發人員應該預期會在沒有先驅滑鼠點擊事件的情況下接收滑鼠滾輪事件。 例如，它們不應該在註冊滑鼠點擊之後接聽滑鼠滾輪事件。 同樣地，桌面應用程式不應該嘗試抓取滑鼠滾輪事件 (例如，藉由在具有鍵盤焦點的情況下設定低層級的勾點) 。

## <a name="tests"></a>測試

Store 應用程式開發人員應該在 Windows 8.1 上進行測試，以確認當滑鼠停留在應用程式上時，所有的滾動功能都能運作。 傳統型應用程式開發人員應該在 Windows 8.1 上測試，以確認這些應用程式不會 (每個指導方針來捕捉滑鼠滾輪事件。 ) 

 

 




