---
title: 隨選安裝的 Windows 元件
description: 隨選安裝的 Windows 元件
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024224"
---
# <a name="windows-components-installed-on-demand"></a>隨選安裝的 Windows 元件

## <a name="platform"></a>平台

**用戶端-** Windows 8.1  







## <a name="description"></a>Description

Windows 8.1： DirectPlay 和 NTVDM 將依需求安裝兩個 Windows 元件。 這些元件會列在 [舊版元件] 節點下的 [選用元件] 中。 這些元件會在本機安裝為作業系統的一部分，並壓縮為選用元件。 當應用程式參考或呼叫其中一個元件時 (通常是在第一次啟動應用程式) 時自動觸發安裝。 使用者將會收到安裝元件的通知，且必須確認動作才能繼續。 如果使用者不是系統管理員，則需要提高許可權才能順利完成。 初始安裝之後，使用者不需要執行任何其他動作，也可以再次使用該元件。

## <a name="manifestation"></a>表現

當應用程式在第一次啟動) 時，于選用元件中參考或呼叫舊版元件 (時，應用程式將會暫停，並會開啟 [視需要提供功能] 對話方塊，要求使用者安裝元件的許可權。 如果使用者按一下 [確定]，他們也可能會看到提高許可權提示，其中必須輸入其認證。 然後會安裝元件，然後應用程式會繼續執行。

## <a name="mitigation"></a>降低

若要讓功能隨選 UI 開啟，您可以使用 DISM 或選擇性元件 UI 來預先安裝 DirectPlay 和 NTVDM。

## <a name="solution"></a>解決方法

強烈建議您避免在未來的應用程式版本中，參考或呼叫已列為 Windows 舊版選用元件的元件。 舊版的選擇性元件只會包含較舊且較少使用的元件，而這些元件可能會造成使用者的效能和安全性問題。

## <a name="tests"></a>測試

不需要額外的測試住宿來提供相容性。 請務必注意，當呼叫或參考選擇性元件時，此對話方塊會出現，而且此安裝需要提高許可權。

 

 




