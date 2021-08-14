---
title: 用戶端應用程式結構
description: Windows 生物特徵辨識架構 API 所支援的用戶端應用程式開發結構。
ms.assetid: ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73
keywords:
- Windows生物特徵辨識架構 api Windows 生物特徵辨識架構 API、用戶端應用程式結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e556bfe7f9f8ac561d9ad22f24b6c2dab16c81acc601dee7456a942cf38deae9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993908"
---
# <a name="client-application-structures"></a>用戶端應用程式結構

Windows 生物特徵辨識架構 API 開發用戶端應用程式時，支援下列結構。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                        | 描述                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**WINBIO \_ 反 \_ 詐騙 \_ 原則**](winbio-anti-spoof-policy.md)<br/>                   | 表示使用者的 lnk-antispoofing 原則。<br/>                                                                       |
| [**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)<br/>                              | 包含非同步作業的結果。<br/>                                                                   |
| [**WINBIO \_ BDB \_ ANSI \_ 381 \_ 標頭**](winbio-bdb-ansi-381-header.md)<br/>              | 指定一系列指紋或棕櫚範例的相關資訊。<br/>                                                 |
| [**WINBIO \_ BDB \_ ANSI \_ 381 \_ 記錄**](winbio-bdb-ansi-381-record.md)<br/>              | 包含來自終端使用者的單一指紋或棕櫚範例的相關資訊。<br/>                                     |
| [**WINBIO \_ BIR**](winbio-bir.md)<br/>                                                 | 代表 (BIR) 的生物特徵辨識資訊記錄。<br/>                                                                     |
| [**WINBIO \_ BIR \_ 資料**](winbio-bir-data.md)<br/>                                      | 指定生物特徵辨識資訊區塊的大小（以位元組為單位）和位移。<br/>                                    |
| [**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)<br/>                                  | 包含 (BIR) 的生物特徵辨識資訊記錄標頭。<br/>                                                         |
| [**WINBIO \_ BSP \_ 架構**](winbio-bsp-schema.md)<br/>                                  | 描述生物特徵辨識服務提供者的功能。<br/>                                                          |
| [**WINBIO \_ 延伸 \_ 引擎 \_ 資訊**](winbio-extended-engine-info.md)<br/>             | 包含生物特徵辨識裝置引擎介面卡的功能和註冊需求相關資訊。<br/>  |
| [**WINBIO \_ 延伸 \_ 註冊 \_ 狀態**](winbio-extended-enrollment-status.md)<br/> | 包含正在進行中之註冊狀態的其他相關資訊。<br/>                               |
| [**WINBIO \_ 擴充的 \_ 感應器 \_ 資訊**](winbio-extended-sensor-info.md)<br/>             | 包含生物特徵辨識設備之感應器介面卡的功能和註冊需求相關資訊。<br/>  |
| [**WINBIO \_ 延伸 \_ 儲存體 \_ 資訊**](winbio-extended-storage-info.md)<br/>           | 包含生物識別設備之儲存體介面卡的功能和註冊需求相關資訊。<br/> |
| [**WINBIO \_ 事件**](winbio-event.md)<br/>                                             | 包含引發事件通知時，傳送至回呼常式的狀態資訊。<br/>                             |
| [**WINBIO 身分 \_ 識別**](winbio-identity.md)<br/>                                       | 包含與生物識別範本相關聯的識別值。<br/>                                                  |
| [**WINBIO \_ 狀態**](winbio-presence.md)<br/>                                       | 包含正在監視的個人是否存在的相關資訊。<br/>                          |
| [**WINBIO \_ 註冊的 \_ 格式**](winbio-registered-format.md)<br/>                    | 將已註冊的資料格式指定為擁有者/格式組。<br/>                                                          |
| [**WINBIO \_ 儲存體 \_ 架構**](winbio-storage-schema.md)<br/>                          | 描述生物特徵辨識存儲裝置配接器的功能。<br/>                                                           |
| [**WINBIO \_ 單元 \_ 架構**](winbio-unit-schema.md)<br/>                                | 描述生物特徵辨識設備的功能。<br/>                                                                      |
| [**WINBIO \_ 版本**](winbio-version.md)<br/>                                         | 包含生物特徵辨識服務提供者元件的軟體版本號碼。<br/>                                      |



 

 

 





