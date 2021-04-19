---
description: Windows 可攜式裝置支援下列物件屬性。
ms.assetid: 29f455d4-6753-42cb-8c18-b50dcb3e71d9
title: '物件屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Object
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6503f4a6d198f0685d6aa35bf9c6058d220eed4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984824"
---
# <a name="object-properties"></a>物件屬性

Windows 可攜式裝置支援下列物件屬性。



| 屬性                                                                                                                                    | VarType         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 物件 \_ 反向 \_ 參考**                                                                                                           | **VT \_ 不明** | VT [](iportabledevicepropvariantcollection.md) LPWSTR 類型的 IPortableDevicePropVariantCollection \_ ，表示 objectid 的清單。 當容器物件參考物件（例如播放清單所參考的音訊物件）時，參考的物件會使用這個屬性來回頭參考其容器物件。 在此範例中，音訊物件可能會回頭參考播放清單物件。                                                                                                                   |
| **WPD \_ 物件 \_ 可以 \_ 刪除**                                                                                                                | **VT \_ BOOL**    | 指定是否可以刪除指定物件的布林值。                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼**                                                                                          | **VT \_ LPWSTR**  | 包含這個物件之最接近功能物件的物件識別碼。 例如，儲存功能物件內的檔案會將這個屬性設定為儲存體功能物件的識別碼。                                                                                                                                                                                                                                                                                                                        |
| <span id="wpd_object_content_type"></span><span id="WPD_OBJECT_CONTENT_TYPE"></span>**WPD \_ 物件 \_ 內容 \_ 類型**                          | **VT \_ CLSID**   | 識別此物件之泛型型別的 **GUID** ，例如檔或電子郵件。 這可以是 Windows 可攜式裝置或自訂驅動程式內容類型 [所定義的物件類型](requirements-for-objects.md)。 裝置物件是唯一不會報告這個屬性的物件。                                                                                                                                                                                                                        |
| <span id="wpd_object_date_authored"></span><span id="WPD_OBJECT_DATE_AUTHORED"></span>**撰寫的 WPD \_ 物件 \_ 日期 \_**                       | **VT \_ 日期**    | 值，指定建立內容的日期和時間。 這可能與檔案的建立日期不同。 例如，音樂檔案具有錄製音樂的製作日期，但在裝置上實際建立 WMA 檔案的建立日期。                                                                                                                                                                                                                                |
| <span id="wpd_object_date_created"></span><span id="WPD_OBJECT_DATE_CREATED"></span>**已 \_ 建立 WPD 物件 \_ 日期 \_**                          | **VT \_ 日期**    | 值，指定在裝置上建立物件的日期和時間。                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="wpd_object_date_modified"></span><span id="WPD_OBJECT_DATE_MODIFIED"></span>**修改的 WPD \_ 物件 \_ 日期 \_**                       | **VT \_ 日期**    | 值，指定在裝置上修改物件的日期和時間。                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="wpd_object_format"></span><span id="WPD_OBJECT_FORMAT"></span>**WPD \_ 物件 \_ 格式**                                             | **VT \_ CLSID**   | 識別物件資料格式的 **GUID** 。 這可以是 [Windows 可攜式裝置](object-format-guids.md) 或自訂驅動程式格式所定義的格式。                                                                                                                                                                                                                                                                                                                                                            |
| **WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_**                                                                                        | **VT \_ BOOL**    | 布林值，指定是否應該從預設資源資料建立此物件的縮圖影像。這可讓沒有縮圖資源的物件提供更容易的流覽體驗。 使用此旗標可能會影響第一個顯示回應，因為應用程式必須從裝置取出並計算縮圖影像。如果可能的話，請更有效率地提供個別的縮圖影像資源。<br/>                                                  |
| **WPD \_ 物件 \_ 提示 \_ 位置 \_ 顯示 \_ 名稱**                                                                                              | **VT \_ LPWSTR**  | 如果指定的物件顯示為提示位置，這個屬性會指出要顯示的提示特定名稱，而非物件名稱。 驅動程式可以指定各種內容類型的位置提示。 您可以將這些檔案視為最上層資料夾物件的快捷方式，其中包含指定之類型的物件。 使用這些位置提示的用戶端可能會顯示與資料夾的物件名稱不同之快捷方式的名稱。 如果這個屬性不存在，通常會改用 **WPD \_ 物件 \_ 名稱** 。 |
| <span id="wpd_object_id"></span><span id="WPD_OBJECT_ID"></span>**WPD \_ 物件 \_ 識別碼**                                                         | **VT \_ LPWSTR**  | 可在裝置上唯一識別物件的字串識別碼。 此識別碼不需要儲存在會話中。如果這個屬性是唯一且持續性的，驅動程式可能會將 **WPD \_ 物件持續性 \_ \_ 唯一 \_ 識別碼** 和 **WPD \_ 物件 \_ 識別碼** 設定為相同的值。<br/>                                                                                                                                                                                                                                                 |
| <span id="wpd_object_is_drm_protected"></span><span id="WPD_OBJECT_IS_DRM_PROTECTED"></span>**WPD \_ 物件 \_ 受到 \_ DRM \_ 保護**             | **VT \_ BOOL**    | 指定媒體資料是否受 DRM 保護的布林值。 如果不存在，則會假設為 False。                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="wpd_object_ishidden"></span><span id="WPD_OBJECT_ISHIDDEN"></span>**WPD \_ 物件 \_ ISHIDDEN**                                       | **VT \_ BOOL**    | 指定是否應該隱藏物件的布林值。 如果不存在，則會假設物件不是隱藏的。                                                                                                                                                                                                                                                                                                                                                                                                     |
| **WPD \_ 物件 \_ 可以 \_ 刪除**                                                                                                                | **VT \_ BOOL**    | 指定是否可刪除物件的布林值。                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="wpd_object_issystem"></span><span id="WPD_OBJECT_ISSYSTEM"></span>**WPD \_ 物件 \_ ISSYSTEM**                                       | **VT \_ BOOL**    | 布林值，指定物件是否代表系統資料 (例如系統檔案) 。 如果不存在，則會假設物件不是系統物件。                                                                                                                                                                                                                                                                                                                                                              |
| <span id="wpd_object_keywords"></span><span id="WPD_OBJECT_KEYWORDS"></span>**WPD \_ 物件 \_ 關鍵字**                                       | **VT \_ LPWSTR**  | 字串，包含與此物件相關聯之以空格分隔的關鍵字清單。                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **WPD \_ 物件 \_ 語言 \_ 地區設定**                                                                                                           | **VT \_ LPWSTR**  | 字串我會 dentifies 指定物件所使用的語言。 如果此物件中包含多個語言，則應該識別主要語言。 這個屬性可包含語言代碼，如 ISO-639 所定義，例如： "en"。 它也可能包含語言國家/地區代碼，此程式碼包含兩個或三個字元的語言代碼（如 ISO-639 標準中所定義），後面接著連字號，然後是在 ISO-3166 中定義的國家/地區代碼，例如： "en-us"。                                |
| <span id="wpd_object_name"></span><span id="WPD_OBJECT_NAME"></span>**WPD \_ 物件 \_ 名稱**                                                   | **VT \_ LPWSTR**  | 物件的顯示名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="wpd_object_non_consumable"></span><span id="WPD_OBJECT_NON_CONSUMABLE"></span>**不可取用的 WPD \_ 物件 \_ \_**                    | **VT \_ BOOL**    | 布林值，指定此物件是否要被辨識或只由裝置儲存。 如果這個屬性不存在，則會假設所有資料都是供取用。                                                                                                                                                                                                                                                                                                                            |
| <span id="wpd_object_original_file_name"></span><span id="WPD_OBJECT_ORIGINAL_FILE_NAME"></span>**WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱**       | **VT \_ LPWSTR**  | 檔案的字串名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="wpd_object_parent_id"></span><span id="WPD_OBJECT_PARENT_ID"></span>**WPD \_ 物件 \_ 父 \_ 識別碼**                                   | **VT \_ LPWSTR**  | 父物件的物件識別碼。 唯一可針對此值傳回空字串的物件是根裝置物件。若要修改此屬性，請呼叫 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) (**WPD \_ 命令 \_ 儲存體 \_ 移動**) 。<br/>                                                                                                                                                                                                                                                    |
| <span id="wpd_object_persistent_unique_id"></span><span id="WPD_OBJECT_PERSISTENT_UNIQUE_ID"></span>**WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼** | **VT \_ LPWSTR**  | 可在裝置上唯一識別物件的字串識別碼，類似于 **WPD \_ 物件 \_ 識別碼**，但必須儲存在會話中。如果物件識別碼 **WPD \_ 物件 \_** 識別碼是唯一且持續性的，驅動程式可能會將 **WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼** 和 **WPD \_ 物件 \_ 識別碼** 設定為相同的值。<br/>                                                                                                                                                                          |
| <span id="wpd_object_references"></span><span id="WPD_OBJECT_REFERENCES"></span>**WPD \_ 物件 \_ 參考**                                 | **VT \_ 不明** | [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) ，其中包含 \_ 可識別參考物件之 VT LPWSTR 物件識別碼的集合。 只有當物件是參考物件（例如資料夾或播放清單）時，才需要此項。                                                                                                                                                                                                                                                            |
| <span id="wpd_object_size"></span><span id="WPD_OBJECT_SIZE"></span>**WPD \_ 物件 \_ 大小**                                                   | **VT \_ UI8**     | 物件資源資料的大小。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="wpd_object_sync_id"></span><span id="WPD_OBJECT_SYNC_ID"></span>**WPD \_ 物件 \_ 同步 \_ 識別碼**                                         | **VT \_ LPWSTR**  | 用戶端所建立的不透明字串，用來保留會話之間的狀態，而不保留已連線裝置內容的目錄。                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




