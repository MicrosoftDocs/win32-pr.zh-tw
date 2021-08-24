---
description: 下表說明適用于 \_ 針對紅外線資料關聯 (IrDA) 位址系列（ (AF \_ IrDA) 和紅外線連結管理通訊協定 (IRLMP) 中所建立之通訊端的 SOL IRLMP 通訊端選項。
ms.assetid: 0457159d-8509-435c-8f57-752530d5df65
title: 'SOL_IRLMP 通訊端選項 (Af \_ irda. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2be68bc658cd7d55ff72a77b6ec87568c37d6d786d0a5e654e9276378b837c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860728"
---
# <a name="sol_irlmp-socket-options"></a>SOL \_ IRLMP 通訊端選項

下表說明適用于針對紅外線資料關聯 (IrDA) 位址系列（ (AF IrDA) 和紅外線連結管理通訊協定 (IRLMP) 中所建立之通訊端的 **SOL \_ IRLMP** 通訊端選項 \_ 。 如需取得和設定通訊端選項的詳細資訊，請參閱 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數參考頁面。

若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)或 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 函數。

<dl> <dt><span id="SOL_IRLMP_Socket_Options"></span><span id="sol_irlmp_socket_options"></span><span id="SOL_IRLMP_SOCKET_OPTIONS"></span>**SOL \_ IRLMP 通訊端選項**</dt> <dd> <dl> <dt> 

| 選項                 | Get | 集合 | Optval 類型     | 描述                                                            |
|------------------------|-----|-----|-----------------|------------------------------------------------------------------------|
| IRLMP \_ 探索 \_ 模式 |     |     |                 |                                                                        |
| IRLMP \_ ENUMDEVICES     | 是 |     | **DEVICELIST**  | 傳回範圍內支援 IR 之裝置的 IrDA 裝置識別碼清單。 |
| IRLMP \_ 獨佔 \_ 模式 |     |     | DWORD (布林值)  | 設定通訊端以略過 TinyTP 圖層，以直接與 IrLMP 通訊。 |
| IRLMP \_ IAS \_ 查詢      | 是 |     | **IAS \_ 查詢**  | 針對指定的服務和其屬性的類別名稱查詢 IAS。      |
| IRLMP \_ IAS \_ 設定        |     | 是 | **IAS \_ 設定**    | 將指定類別名稱和屬性的屬性值設定為 IAS。 |
| IRLMP \_ IRLPT \_ 模式     |     | 是 | DWORD (布林值)  | 可與支援 IR 的印表機進行通訊。                        |
| IRLMP \_ 參數      |     |     |                 |                                                                        |
| IRLMP \_ 傳送 \_ PDU \_ LEN  | 是 |     | DWORD           | 捕獲使用 IRLMP 9WIRE 模式所需的最大 PDU 長度 \_ \_ 。   |
| IRLMP \_ 銳利 \_ 模式     |     | 是 |                 |                                                                        |
| IRLMP \_ TINYTP \_ 模式    |     | 是 |                 |                                                                        |
| IRLMP \_ 9WIRE \_ 模式     | 是 | 是 | DWORD (布林值)  | 將 IrDA 通訊端置於 IrCOMM 模式。                                 |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_IRLMP_options"></span><span id="windows_support_for_sol_irlmp_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_IRLMP_OPTIONS"></span>**Windows支援 SOL \_ IRLMP 選項**</dt> <dd> <dl> <dt> 

| 選項                            | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows我，Windows 98 | Windows NT 4.0 |
|-----------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|------------------------|----------------|
| IRLMP \_ 探索 \_ 模式<br/> |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ ENUMDEVICES<br/>     | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ 獨佔 \_ 模式<br/> |           |                     |               |                     |            |              |                        |                |
| IRLMP \_ IAS \_ 查詢<br/>      | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ IAS \_ 設定<br/>        | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ IRLPT \_ 模式<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |
| IRLMP \_ 參數<br/>      |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ 傳送 \_ PDU \_ LEN<br/>  | x         | x                   | x             | x                   | x          | x            |                        |                |
| IRLMP \_ 銳利 \_ 模式<br/>     |           |                     |               |                     |            |              |                        |                |
| IRLMP \_ TINYTP \_ 模式<br/>    |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ 9WIRE \_ 模式<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

**SOL \_ IRLMP** 通訊端選項以及這些通訊端選項所使用的結構會定義在 *Af \_ irda .h* 標頭檔中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Af \_ irda。h</dt> </dl> |



 

 




