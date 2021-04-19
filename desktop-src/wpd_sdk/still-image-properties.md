---
description: Windows 可攜式裝置支援下列仍為影像的屬性。
ms.assetid: 0b5a126c-5064-48e5-a635-00c3e9ab6a2c
title: '靜止影像屬性 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Still
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3bc06428dc153dc8ff205e283b1000ef0a171b6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992868"
---
# <a name="still-image-properties"></a>靜止影像屬性

Windows 可攜式裝置支援下列仍為影像的屬性。



| 屬性                                                                                                                                                       | VarType        | Description                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 靜止 \_ 影像 \_ 演出者**                                                                                                                                  | **VT \_ LPWSTR** | 裝置的擁有者/使用者名稱。                                                                                                                                                                                                                                                                                    |
| <span id="wpd_still_image_burst_interval"></span><span id="WPD_STILL_IMAGE_BURST_INTERVAL"></span>**WPD \_ 仍然是影像高載 \_ \_ \_ 間隔**                       | **VT \_ UI4**    | 在高載模式映射捕捉中，映射捕獲之間的延遲時間（以毫秒為單位）。                                                                                                                                                                                                                                       |
| <span id="wpd_still_image_burst_number"></span><span id="WPD_STILL_IMAGE_BURST_NUMBER"></span>**WPD \_ 仍然是影像高載 \_ \_ \_ 數目**                             | **VT \_ UI4**    | 在高載模式映射捕捉中，要捕捉的映射數目。                                                                                                                                                                                                                                                              |
| **WPD \_ 仍然是 \_ 映射 \_ 捕捉 \_ 延遲**                                                                                                                          | **VT \_ UI4**    | 指定命令捕獲映射與實際捕獲之間的時間延遲（以毫秒為單位）。                                                                                                                                                                                                                    |
| **WPD \_ 仍然是 \_ 影像 \_ 捕捉 \_ 格式**                                                                                                                         | **VT \_ CLSID**  | 用來捕捉影像的格式。 這是 Windows 可攜式裝置所定義的其中一個 [格式 GUID 值](object-format-guids.md) 。                                                                                                                                                                        |
| <span id="wpd_still_image_capture_mode"></span><span id="WPD_STILL_IMAGE_CAPTURE_MODE"></span>**WPD \_ 仍然是 \_ 影像 \_ 捕捉 \_ 模式**                             | **VT \_ UI4**    | [**WPD \_ capture \_ 模式**](wpd-capture-modes.md)列舉值，指定用來捕捉映射的捕獲模式。                                                                                                                                                                                                    |
| **WPD \_ 仍然是 \_ 映射 \_ 捕獲 \_ 解析**                                                                                                                     | **VT \_ LPWSTR** | 字串，指定要捕捉的影像大小。 映射大小是以圖元為單位指定，格式為「*寬度* x *高度*」。 例如：「800x600」。                                                                                                                                                                          |
| **WPD \_ 靜止 \_ 影像 \_ 壓縮 \_ 設定**                                                                                                                    | **VT \_ UI8**    | 描述在捕獲映射時所使用的影像壓縮設定。 這是裝置特定的。                                                                                                                                                                                                                     |
| **WPD \_ 靜止 \_ 影像 \_ 對比**                                                                                                                                | **VT \_ UI4**    | 數位，指定在捕獲影像時要套用的對比設定，其中零是最小的對比，而較大的數位表示較高的對比。                                                                                                                                                            |
| **WPD \_ 仍 \_ 影像 \_ 數位 \_ 縮放**                                                                                                                           | **VT \_ UI4**    | 數位，指定在捕獲影像時要使用的數位縮放量。 此數位為1或更高，以10的因數進行縮放。 值為 1 (代表 10) 表示無數位縮放;代表 20) 的值為 2 (表示) 會捕獲1倍的影像 (1/4 的影像。                  |
| **WPD \_ 靜止 \_ 影像 \_ 效果 \_ 模式**                                                                                                                            | **VT \_ UI4**    | [**WPD \_ 效果 \_ 模式**](wpd-effect-modes.md)列舉值，指定在捕獲影像時要使用的影像效果。                                                                                                                                                                                                   |
| **WPD \_ 仍 \_ 影像 \_ 曝光 \_ 偏差 \_ 補償**                                                                                                            | **VT \_ UI4**    | 指定頂點單位的數位，以調整曝光。 單位為停止 x 1000。 指定零表示原廠預設值。                                                                                                                                                                                       |
| **WPD \_ 仍然是 \_ 影像 \_ 曝光 \_ 索引**                                                                                                                         | **VT \_ UI4**    | 數位，指定在捕獲影像時要模擬的 ISO 電影速度。 0xFFFF 的值表示應該自動設定這個值。                                                                                                                                                                      |
| **WPD \_ 仍然是 \_ 影像 \_ 曝光 \_ 計量 \_ 模式**                                                                                                                | **VT \_ UI4**    | [**WPD 的 \_ 曝光 \_ 計量 \_ 模式**](wpd-exposure-metering-modes.md)列舉值，指定要在捕獲映射時使用的計量模式。                                                                                                                                                                          |
| <span id="wpd_still_image_exposure_program_mode"></span><span id="WPD_STILL_IMAGE_EXPOSURE_PROGRAM_MODE"></span>**WPD \_ 靜止 \_ 影像 \_ 曝光 \_ 程式 \_ 模式** | **VT \_ UI4**    | [**WPD \_ 曝光 \_ 程式 \_ 模式**](wpd-exposure-program-modes.md)列舉值，指定在捕獲影像時要使用的曝光程式。                                                                                                                                                                         |
| **WPD \_ 仍然是 \_ 影像 \_ 曝光 \_ 時間**                                                                                                                          | **VT \_ UI4**    | 在捕獲映射時所要使用的快門速度，以秒為單位 x 10000。                                                                                                                                                                                                                                                       |
| **WPD \_ 靜止 \_ 影像 \_ 閃爍 \_ 模式**                                                                                                                             | **VT \_ UI4**    | [**WPD \_ flash \_ 模式**](wpd-flash-modes.md)列舉值，指定在捕獲影像時要使用的閃爍模式。                                                                                                                                                                                                      |
| **WPD \_ 仍為 \_ 影像 \_ FNUMBER**                                                                                                                                 | **VT \_ UI4**    | 在捕獲影像時指定鏡頭光圈的數位。 此數位是 f-stop 數位 100 (因此14會指出 f/1.4) 。只有當 [WPD 仍為 [ \_ \_ 影像 \_ 曝光 \_ 程式 \_ 模式]](/windows) 設定為 [手動] 或 [光圈先決級] 時，這個屬性才有效。<br/> |
| **WPD \_ 仍為 \_ 影像 \_ 焦點 \_ 長度**                                                                                                                           | **VT \_ UI4**    | 捕捉影像時要使用的焦長度（以毫米 x 100 為單位）。 例如，35mm 會是3500。                                                                                                                                                                                                                 |
| **WPD \_ 仍 \_ 影像 \_ 焦點 \_ 距離**                                                                                                                         | **VT \_ UI4**    | 裝置應該使用的焦點距離（以毫米為單位）。 0xFFFF 的值表示 (超過655計量) 的無限焦點。                                                                                                                                                                                              |
| **WPD \_ 仍然是 \_ 影像 \_ 焦點 \_ 計量 \_ 模式**                                                                                                                   | **VT \_ UI4**    | [**WPD \_ 焦點 \_ 計量 \_ 模式**](wpd-focus-metering-modes.md)列舉值，指定影像捕獲裝置在決定如何將焦點放在主題時，應使用的焦點模式。                                                                                                                                     |
| **WPD \_ 仍為 \_ 影像 \_ 焦點 \_ 模式**                                                                                                                             | **VT \_ UI4**    | [**WPD \_ 焦點 \_ 模式**](wpd-focus-modes.md)列舉值，指定在捕獲影像時要使用的焦點模式。                                                                                                                                                                                                      |
| **WPD \_ 仍 \_ 影像 \_ RGB \_ 增益**                                                                                                                               | **VT \_ LPWSTR** | 以 null 終止的字串，指定在捕獲影像時要使用的 RGB 增益。 字串是三個以分號分隔的數位，不含中間的空格，格式為 "*R*：*G*：*B*"。                                                                                                                                    |
| **WPD \_ 仍 \_ 影像 \_ 清晰度**                                                                                                                               | **VT \_ UI4**    | 指定在捕獲影像時要使用之清晰度的數位，其中0是最少的最小值，而較大的數位表示增加清晰度。                                                                                                                                                                        |
| <span id="wpd_still_image_timelapse_interval"></span><span id="WPD_STILL_IMAGE_TIMELAPSE_INTERVAL"></span>**WPD \_ 仍然是 \_ 影像 \_ TIMELAPSE \_ 間隔**           | **VT \_ UI4**    | 映射捕獲在時間間隔中的時間延遲（以毫秒為單位）。                                                                                                                                                                                                                                        |
| <span id="wpd_still_image_timelapse_number"></span><span id="WPD_STILL_IMAGE_TIMELAPSE_NUMBER"></span>**WPD \_ 仍然是 \_ 影像 \_ TIMELAPSE \_ 數位**                 | **VT \_ UI4**    | 要在時間間隔映射捕捉中捕捉的影像數目。                                                                                                                                                                                                                                                          |
| **WPD \_ 仍然是 \_ 影像 \_ 上傳 \_ URL**                                                                                                                             | **VT \_ LPWSTR** | 指定裝置在捕獲映射後，應將其傳送至其中的 URL。                                                                                                                                                                                                                                                 |
| **WPD \_ 仍 \_ 影像的 \_ 白色 \_ 餘額**                                                                                                                          | **VT \_ UI4**    | [**WPD 的 \_ 白色 \_ 餘額 \_ 設定**](wpd-white-balance-settings.md)列舉值，指定在捕獲影像時要使用的白色餘額設定。                                                                                                                                                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

