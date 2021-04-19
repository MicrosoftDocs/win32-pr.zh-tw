---
description: Windows 可攜式裝置支援下列事件屬性。
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: '事件屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998684"
---
# <a name="event-properties"></a>事件屬性

Windows 可攜式裝置支援下列事件屬性。



<table>
<thead>
<tr class="header">
<th>屬性</th>
<th>VarType</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>保留供未來使用。</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>布林值，指定是否要將事件廣播至所有用戶端。用戶端可以藉由向 <strong>IPortableDevice：： Advise</strong>註冊回呼，來接收此事件。<br/></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>布林值，指定物件的子階層是否已變更。這個參數是用來通知呼叫端，已新增或移除指定之物件的某些子系。 通常會在裝置端起始階層變更。 用戶端可能必須重新列舉這個資料夾的子系，才能讓他們的觀點保持在最新狀態。<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></td>
<td><strong>VT_CLSID</strong></td>
<td>識別事件的值。</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>當 cookie 透過呼叫 <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent：： CreateObjectWithPropertiesAndData</strong></a> 方法要求建立物件時，會將 cookie 回傳給用戶端。加入這個參數是為了方便呼叫者將已加入物件的事件系結至它所傳送的要求，以建立物件。 驅動程式會在處理<strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong>命令時，將此 cookie 回傳為<strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong>傳回值。<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>可唯一識別父物件的值。 這個屬性類似于 <strong>WPD_OBJECT_PARENT_ID</strong>，但此識別碼不會在會話之間變更。</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></td>
<td><strong>VT_UI4</strong></td>
<td>值，指定目前執行中作業的進度。 這個屬性的值的範圍可以從0到100，而100則表示作業已完成。</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>值，指出作業的目前狀態，例如，已啟動、執行中、已停止等等。這個參數的可能值是來自 PortableDevice 中定義的 <strong>WPD_OPERATION_STATES</strong> 列舉。 可能的值包括：<br/> <dl> <strong>WPD_OPERATION_STATE_UNSPECIFIED</strong><br />
<strong>WPD_OPERATION_STATE_STARTED</strong><br />
<strong>WPD_OPERATION_STATE_RUNNING</strong><br />
<strong>WPD_OPERATION_STATE_PAUSED</strong><br />
<strong>WPD_OPERATION_STATE_CANCELLED</strong><br />
<strong>WPD_OPERATION_STATE_FINISHED</strong><br />
<strong>WPD_OPERATION_STATE_ABORTED</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>值，指定產生事件的裝置。這是隨插即用 (PnP) 系統所提供的裝置或服務識別碼，與 <strong>IPortableDevice：： open</strong>或 <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService：： open</strong></a> 方法中使用的字串相同。<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>WPD 驅動程式用來識別裝置服務方法之作業的字串。 應用程式不應直接使用此參數。</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




