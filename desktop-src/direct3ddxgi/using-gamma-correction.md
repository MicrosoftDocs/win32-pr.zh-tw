---
description: Gamma 更正（簡稱為 gamma）是指系統用來編碼和解碼影像中圖元值的非線性運算名稱。
ms.assetid: 97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A
title: 使用 gamma 更正
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c5f5d3af8550f86280e6203858444469a5aa8caaab462f560da152caaa2a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288960"
---
# <a name="using-gamma-correction"></a>使用 gamma 更正

Gamma 更正（簡稱為 gamma）是指系統用來編碼和解碼影像中圖元值的非線性運算名稱。

-   [什麼是 gamma？是什麼？](#what-is-gamma-and-what-is-it-for)
-   [Windows 上的 gamma 背景](#background-of-gamma-on-windows)
-   [顯示器硬體的演進](#evolution-of-display-hardware)
-   [DXGI 中的 Gamma 控制項功能](#gamma-control-capabilities-in-dxgi)
-   [使用 DXGI 設定 gamma 控制項](#setting-gamma-control-with-dxgi)
-   [Gamma 控制項 practicalities](#gamma-control-practicalities)
-   [相關主題](#related-topics)

## <a name="what-is-gamma-and-what-is-it-for"></a>什麼是 gamma？是什麼？

在圖形管線的結尾，只要影像離開電腦，讓它沿著監視器纜線進行，就有一小部分的硬體可以即時轉換圖元值。 此硬體通常會使用查閱資料表來轉換圖元。 此硬體使用來自表面的紅色、綠色和藍色值來查閱資料表中的 gamma 修正值，然後將更正的值傳送至監視器，而不是實際的介面值。 因此，這個查閱資料表是以任何其他色彩取代任何色彩的機會。 雖然資料表具有這一層級的電源，但一般使用方式是稍微調整影像，以補償監視器回應的差異。 監視器的回應是一種函式，它會將圖元的紅色、綠色和藍色元件的數值與圖元顯示的亮度建立關聯。

這就是這個資料表的目的，但是遊戲開發人員發現它有創意的用途，例如將整個螢幕的螢幕閃爍為紅色以心理效果。 在新式遊戲應用程式中，在每個畫面格的後續處理過程中，我們通常會提供其他方法來進行這類作業。 事實上，我們建議您只保留 gamma 資料表，因為它可能會用來校正監視器的回應，而對 gamma 的變化，對 gamma 的變化會損毀這項仔細的校正。

判斷 gamma 校正的科學是很複雜的，在這裡並不會顯示，而是除了用來照亮名稱 "gamma" 的位置。 CRT (也就是舊的半透明玻璃) 監視器的回應是一個複雜的函式，但這些監視器的物理意思表示這些監視器所呈現的回應可以初步由這個 power 函數表示：

亮度 ( 輸入 ) = 輸入<sup>gamma</sup>

Gamma 值通常接近2.0 的值。 LCD 監視器和其他所有較新的技術都是特別設計來呈現類似的回應，因此我們不需要為這些新技術 recalibrated 所有的軟體和映射。 SRGB 標準宣告此 gamma 值正好是2.2，而此值已成為廣泛實行的標準。

人類眼也有一個回應函式，其大約會反轉 CRT 電源函式。 這表示，圖元的感覺亮度在該圖元的 RGB 值上大致上會呈線性。

由於 gamma 值2.2 已經成為一種被忽略的標準，因此我們通常不需要擔心此資料表中編碼的 gamma 曲線太多，而且可以將它保留為線性、一對一的對應。 當然，適當的色彩比對需要 exquisite 此功能，但該討論已超出本主題的範圍。 Windows 包含一種工具，可讓使用者將其顯示內容調整為 gamma 2.2，而此工具會使用查閱資料表硬體，為其電腦衍生出謹慎選擇的微妙調整。 使用者可以藉由搜尋「校正色彩」來執行此工具。 針對將此程式自動化的特定監視器，也有妥善定義的色彩設定檔。 「校正色彩」工具可以偵測這些較新的監視器，並通知使用者已在進行校正。

這種將 power 定律編碼成色彩值的概念，在圖形管線中的其他地方很有用，尤其是在材質中。 針對材質，您希望較深的色彩有更高的精確度，因為我們剛剛提到的是對數人類眼的回應。 在管線的這個部分中小心處理 gamma 是很重要的。 如需詳細資訊，請參閱 [轉換色彩空間的資料](converting-data-color-space.md)。

本主題的其餘部分只著重于管線最後一部分（框架緩衝區資料和監視器）之間的 gamma 修正。 如果您想要撰寫校正 wizard 或在全螢幕應用程式中建立特殊效果，其中的後置處理步驟並不實用，以下是您需要的資訊。

## <a name="background-of-gamma-on-windows"></a>Windows 上的 gamma 背景

Windows 的電腦通常有一個 gamma 資料表，此資料表是採用三個位元組並輸出三個位元組的查閱資料表。 這些 triplet 是 768 (256 x 3) 個位元組的 RAM。 當您的顯示格式包含三個 RGB 位元組值，但無法描述當顯示格式的範圍大於 \[ 0、1 \] （例如浮點值）時，您可能想要的轉換，這是不錯的選擇。 在 Windows 中，控制 gamma 的 api 已遵循演進，因為顯示格式已變得更複雜。

提供 gamma 控制項的第一個 Windows api Windows 圖形裝置介面 (GDI) 的 [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp)和 [**GetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-getdevicegammaramp)。 這些 Api 會使用 3 256-entry 陣列，其中每個單字編碼為零，並以單字值0和65535表示。 單字的額外精確度通常不適用於實際的硬體查閱資料表，但是這些 Api 的目的是要有彈性。 這些 Api 相對於本節稍後所述的其他 Api，只允許來自身分識別函式的小偏差。 事實上，這一條的任何專案都必須在識別值的32768內。 這種限制表示沒有任何應用程式可以將顯示器完全變為黑色或其他無法閱讀的色彩。

下一個 API 是 Microsoft Direct3D 9 的 [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)，其遵循與 [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp)相同的模式和資料格式。 Direct3D 9 gamma 曲線的預設值並不特別有用;雖然 API 是以0-65535 來定義的，但它是一種初始化為0-255 而非0-65535 的單字。

最新的 API 是 [**IDXGIOutput：： SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol)。 此 API 有更具彈性的配置，可表示 gamma 控制項，因為適用 DXGI 增加了一組顯示格式，包括每個通道10個整數位、16位浮點數格式，以及 XR \_ 偏差延伸範圍格式。

這些 Api 全都在相同的硬體上運作，並且變更相同的值。 Direct3D 9 和 DXGI Api 都是「僅限寫入」。 您無法讀取硬體的值、加以修改，然後設定它。 您只能設定滑軌。 此外，您只能在應用程式全螢幕時，設定 gamma。 這項限制是保證桌面永遠可讀取的另一種方式。 也就是說，應用程式可以打擾自己的顯示，但 Windows 會在應用程式失去全 (螢幕時，還原先前的 gamma 曲線，例如，透過 alt-tab 或 ctrl-alt-del) 。

## <a name="evolution-of-display-hardware"></a>顯示器硬體的演進

有些較新的監視器可能會顯示各種濃度。 但是，當顯示格式只能代表0和1之間的值時，顯示器必須將零對應至其最深的值，並將其對應至其最亮的值。 這個最亮的值可能太亮，可方便您在白色背景上以黑色文字來觀賞網頁，但很適合用於明亮的特殊效果，例如，從 lake 觀看陽光 glittering，或從天空中的閃電。 因此，我們需要一種方式來表達這些更廣泛的範圍。 DXGI 1.1 和更新版本包含顯示格式值，可讓1.0 代表舒適的白色值，並保留更寬的顯示格式值以獲得過度的特殊效果。 DXGI 1.1 支援兩種顯示格式，可表達這些較大的值： DXGI \_ 格式 \_ R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM 和16位浮點數。 如需這些格式的完整討論，請參閱 [延伸格式的詳細資料](/windows-hardware/drivers/display/details-of-the-extended-format)。 接下來，我們將探討為什麼 DXGI 的 [**IDXGIOutput：： SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) gamma API 需要大於1.0 的圖元值。

## <a name="gamma-control-capabilities-in-dxgi"></a>DXGI 中的 Gamma 控制項功能

DXGI 可讓顯示器驅動程式將其 gamma 控制項表示為逐步線性功能。 這個逐步線性函式是由這個函式的控制點、函式可以轉換成的值範圍，以及可在轉換後套用的額外選擇性縮放和位移運算來定義。 應用程式可以呼叫 [**IDXGIOutput：： GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) 方法，以在 [**DXGI \_ GAMMA \_ 控制項 \_ 功能**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) 結構中取得所有這些控制項功能。

此圖表顯示僅有四個控制點的線性函數。

![gamma 更正線性函數](images/gamma-linear-function.png)

DXGI 會依據介面色軸的位置來定義控制點。 在上圖中，控制點的位置是0、0.5、0.75 和1.0。 這些控制點表示硬體可以轉換範圍0到1.0 之間的值。 DXGI 會在 [**DXGI \_ GAMMA \_ 控制項 \_ 功能**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85))的 **ControlPointPositions** 陣列成員中列出這些控制點，並一律以遞增順序宣告它們。 DXGI 只會填滿 **ControlPointPositions** 陣列的第一個元素，並指出具有 **DXGI \_ GAMMA \_ 控制項 \_ 功能** 之 **NumGammaControlPoints** 成員的元素數目。 如果 **NumGammaControlPoints** 小於1025，DXGI 會讓其餘的 **ControlPointPositions** 元素保持未定義狀態。

此圖表所代表的硬體可以將值轉換為0到1.25 的範圍。 因此，DXGI 會分別將 **MinConvertedValue** 和 **MaxConvertedValue** 成員設定為 0.0 f 和 1.25 f。

DXGI 會設定 [**dxgi \_ GAMMA \_ 控制項 \_ 功能**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85))的 **ScaleAndOffsetSupported** 成員，以指出硬體是否支援縮放和位移功能。 如果硬體支援縮放和位移，則會保留簡單的一對一查閱資料表，但接著會調整資料表的輸出，以將輸出延展到大於 \[ 0，1的範圍 \] 。 硬體會先調整取自查閱資料表的值，然後將它們位移。

> [!Note]  
> 連接到同一部電腦的不同監視器可能會有不同的 gamma 控制項功能。 此外，gamma 控制項功能實際上也會隨著輸出的顯示模式而變更。 因此，建議您一律在應用程式進入全螢幕模式之後，呼叫 [**IDXGIOutput：： GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) 來查詢 gamma 控制項功能。

 

您可以使用這些 gamma 控制項功能值來衍生控制項值，然後您可以使用 [**IDXGIOutput：： SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) API 來設定這些值。

## <a name="setting-gamma-control-with-dxgi"></a>使用 DXGI 設定 gamma 控制項

若要設定 gamma 控制項，當您呼叫 [**IDXGIOutput：： SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) API 時，您會將指標傳遞至 [**DXGI \_ gamma \_ 控制項**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85))結構。

您可以設定 [**DXGI \_ GAMMA \_ 控制項**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85))的 **小** 數位數和 **位移** 成員，以指定要將硬體套用至您從查閱資料表取得之值的小數位數和位移值。 您可以安全地將 [ **刻度** ] 設定為1，並將 [ **位移** ] 設為零 (也就是，一個小數位數沒有任何作用，而且如果您不想要使用 [調整] 和 [位移] 功能，或如果硬體沒有該功能，就不會有零的) 影響。

您將 [**dxgi \_ gamma \_ 控制項**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85))的 **GammaCurve** 陣列成員設定為 GAMMA 曲線上點的 [**dxgi \_ RGB**](/previous-versions/windows/desktop/legacy/bb173071(v=vs.85))結構清單。 每個 **DXGI \_ RGB** 元素都會指定代表該點之紅色、綠色和藍色元件的浮點值。 Gamma 曲線不會使用 Alpha 值。 您可以使用從 **NumGammaControlPoints** 的 [**DXGI \_ GAMMA \_ 控制項 \_ 功能**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) 取得的數位，來填入 **GammaCurve** 陣列中的元素數目。 您放在 **GammaCurve** 陣列中的每個元素都是每個控制點的高度。

請注意，在上圖中，您現在可以控制每個控制點的垂直位置，而且您有紅色、綠色和藍色的個別控制項。 例如，您可以將所有綠色和藍色值設定為零，並將紅色值設定為從零到一的遞增樓梯。 在此案例中，顯示的影像只會顯示其紅色部分，藍色和綠色會顯示為黑色。 您也可以為所有色彩設定遞減的樓梯，以產生反向顯示。 您放在 **GammaCurve** 陣列中的任何值，都必須在您從 **MinConvertedValue** 和 **MaxConvertedValue** 的 [**DXGI \_ GAMMA \_ 控制項 \_ 功能**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85))的成員中取得的值內。

## <a name="gamma-control-practicalities"></a>Gamma 控制項 practicalities

只有當應用程式是全螢幕時，才適用 DXGI 的 gamma 控制項。 Windows 會在應用程式結束或返回視窗模式時，還原顯示的先前狀態。 但是，如果應用程式重新進入全螢幕模式，Windows 不會還原您的應用程式 gamma 狀態。 當您的應用程式重新進入全螢幕模式時，必須明確地還原其 gamma 狀態。

並非所有的介面卡都支援 gamma 控制項。 如果介面卡不支援 gamma 控制項，則會忽略呼叫來設定 gamma 的斜坡。

在遠端桌面執行的應用程式無法完全控制 gamma。

如果滑鼠游標在硬體 (中實作為大部分的) ，則通常不會回應 gamma 設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXGI 的程式設計指南](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
