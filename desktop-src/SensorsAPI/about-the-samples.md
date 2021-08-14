---
description: Windows SDK 包含實用的程式碼範例和工具，可協助您瞭解和使用 Windows 感應器和位置平台和相關的 api。
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: 關於範例和工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5eecd388323ae8a548fcfefbc116224125b4b137f85231c56ea66235b3233fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890315"
---
# <a name="about-the-samples-and-tools"></a>關於範例和工具

Windows SDK 包含實用的程式碼範例和工具，可協助您瞭解和使用 Windows 感應器和位置平台和相關的 api。

## <a name="samples"></a>範例

Windows SDK 包含下列感應器 API 範例。 您可以在名為 samples winui 感應器的資料夾中 \\ \\ ，找到 \\ 您安裝 Windows SDK 的感應器 API 範例。 例如，如果您將 Windows SDK 安裝在 c 磁片磁碟機上，您會在下列資料夾中找到範例： C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ winui \\ 感應器。



| 範例名稱       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AmbientLightAware | 此 MFC 範例示範如何使用感應器 API，方法是從電腦上的環境光線感應器讀取資料，並根據光源條件來變更文字大小。 您可以看到顯示如何管理事件，以及如何要求使用者權限的程式碼。 您也可以看到一個範例，說明如何根據不同的光源條件來管理使用者介面。 如需詳細資訊，請參閱 [建立 Light-Aware 使用者介面](creating-light-aware-user-interfaces.md)。<br/> 您必須安裝 Visual Studio 2008 才能建立此範例。<br/> |



 

如需詳細資訊，請參閱範例隨附的名稱為 ReadMe.txt 的檔案。

您也可以從程式碼庫下載 AmbientLightAware 範例。 如需詳細資訊，請參閱 [環境亮感知](/samples/browse/?redirectedfrom=MSDN-samples) 下載頁面。

## <a name="tools"></a>工具

Windows SDK 包含虛擬光線感應器，可用來模擬硬體型光線感應器裝置。 您可以使用此工具，將資料提供給 AmbientLightAware 範例，以查看範例中的程式碼如何運作。

下表說明您必須用來執行虛擬光線感應器的檔案。 您可以在已安裝 Windows SDK 的名稱為 Bin 的資料夾中找到這些檔案。 例如，如果您將 Windows SDK 安裝在32位電腦的 c 磁片磁碟機上，您會在下列資料夾中找到虛擬光線感應器檔案： C： \\ Program files \\ Microsoft sdk Windows v2.0 \\ \\ \\ Bin。 在64位的電腦上，您必須使用64位版本的工具。 在 Windows SDK 中，64位工具位於名為 x64 的子資料夾中。



| 檔案名稱                    | 描述                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| VirtualLightSensor.exe       | 此程式提供滑杆控制項，可讓您變更虛擬感應器所報告的燈光資料層級。 |
| VirtualLightSensorDriver.dll | 模擬燈光感應器的邏輯感應器驅動程式。                                                                       |
| VirtualLightSensorDriver .inf | 虛擬光線感應器驅動程式的 INF 檔案。                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a>安裝虛擬光線感應器

使用虛擬光線感應器應用程式之前，您必須安裝邏輯感應器驅動程式。 請遵循下列步驟：

1.  以系統管理員身分開啟命令視窗。
2.  變更為 Windows SDK Bin 資料夾。
3.  輸入 **pnputil-VirtualLightSensorDriver .inf**。
4.  出現提示時，請按一下 [ **繼續安裝此驅動程式軟體**]。
5.  等候命令視窗報告驅動程式已順利安裝。

### <a name="running-the-virtual-light-sensor"></a>正在執行虛擬光線感應器

若要執行虛擬光線感應器，只要按兩下 .exe 的檔案即可。 當系統提示時，請務必啟用感應器。

當您執行程式時，可能會注意到感應器變成可用之前會有延遲。 虛擬光線感應器使用者介面會在標題列中顯示「等待中」的訊息，而邏輯感應器管理員會為邏輯感應器建立裝置節點。 等候的訊息消失之後，您可以使用滑杆來設定虛擬光線感應器的 lux 輸出等級。

下圖顯示虛擬光線感應器使用者介面處於 [就緒] 狀態。

![虛擬光線感應器使用者介面](images/virtuallightsensor.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於邏輯感應器](about-logical-sensors.md)
</dt> <dt>

[**感應器 \_ 類別 \_ 燈**](sensor-category-light.md)
</dt> </dl>

 

