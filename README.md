# HOTS battlelobby

Structure of "replay.server.battlelobby" for Heroes of the storm replay.
All others file can be found at https://github.com/Blizzard/heroprotocol

Visualization for last version (array of Byte is byte aligned):

      record[:0 + 0]
        Attributes: record[:0 + 0]
          m_cacheFileNames: array [:6 + 0] of array [:10 + 0] of Byte
          m_cacheHandles: array [:6 + 0] of record[:0 + 0]
              m_FileType: array [:0 + 4] of Byte
              m_Realm: array [:0 + 4] of Byte
              m_SHA256Hash: array [:0 + 32] of Byte
            end
          EnabledAttributes: array [:9 + 0] of record[:0 + 0]
              Namespace: Integer(:32 + 0)
              AttrId: Integer(:32 + 0)
              SupportedValues: array [:12 + 0] of record[:0 + 0]
                  ValueName: array [:0 + 32] of bit
                  first: Optional:1 of (record[:0 + 0]
                      f32: Optional:1 of (Integer(:32 + 0))
                      NewField6: Integer(:6 + 0)
                      word: Integer(:16 + 0)
                    end)
                  second: Optional:1 of (record[:0 + 0]
                      f32: Optional:1 of (Integer(:32 + 0))
                      NewField6: Integer(:6 + 0)
                      word: Integer(:16 + 0)
                    end)
                  f70: Optional:1 of (record[:0 + 0]
                      NewField6: Integer(:6 + 0)
                      NewField32: Integer(:32 + 0)
                      NewField16: Integer(:16 + 0)
                      NewField16: Integer(:16 + 0)
                    end)
                  f1: array [:0 + 1] of bit
                  f1: array [:0 + 1] of bit
                  f1: array [:0 + 1] of bit
                end
              EnabledWithAttribs: Optional:1 of (record[:0 + 0]
                  NewField25: array [:0 + 25] of bit
                  AttribsValues: array [:5 + 0] of record[:0 + 0]
                      NewField5: array [:0 + 5] of bit
                      Namespace: Integer(:32 + 0)
                      AttrId: Integer(:32 + 0)
                      Values: array [:12 + 0] of array [:0 + 32] of bit
                    end
                end)
              _end: record[:0 + 0]
                NewField5: array [:0 + 5] of bit
                NewField5: array [:0 + 5] of bit
                NewField5: array [:0 + 5] of bit
                NewField: array [:0 + 32] of bit
                a170: array [:8 + 0] of record[:0 + 0]
                    b5: array [:0 + 5] of bit
                    b165: array [:0 + 165] of bit
                    b15: array [:0 + 15] of bit
                  end
                NewField: record[:0 + 0]
                  b11: array [:0 + 11] of bit
                  f1: array [:0 + 1] of bit
                  b9: array [:0 + 9] of bit
                end
              end
            end
        end
        PlayerSelectedAttributes: record[:0 + 0]
          NewField: array [:0 + 30] of bit
          NewField: Integer(:16 + 0)
          NewField: array [:0 + 81] of bit
          Attributes: array [:9 + 0] of record[:0 + 0]
              Namespace: Integer(:32 + 0)
              AttrId: Integer(:32 + 0)
              Values: case (:8 + 0) of
                GlobalValue(0): record[:0 + 0]
                  ValueIndex: array [:0 + 11] of bit
                  IsSet: array [:0 + 1] of bit
                end
                ByPlayerValue(1): array [:5 + 0] of record[:0 + 0]
                    ValueIndex: array [:0 + 11] of bit
                    IsSet: array [:0 + 1] of bit
                  end
              end
            end
        end
        Locales: record[:0 + 0]
          s2mv: array [:6 + 0] of record[:0 + 0]
              m_FileType: array [:0 + 4] of Byte
              m_Realm: array [:0 + 4] of Byte
              m_SHA256Hash: array [:0 + 32] of Byte
            end
          Langs: array [:5 + 0] of record[:0 + 0]
              Lang: array [:0 + 32] of bit
              s2ml: array [:6 + 0] of record[:0 + 0]
                  m_FileType: array [:0 + 4] of Byte
                  m_Realm: array [:0 + 4] of Byte
                  m_SHA256Hash: array [:0 + 32] of Byte
                end
            end
          fil: array [:0 + 128] of bit
          UsedMods: array [:5 + 0] of record[:0 + 0]
              ModId: record[:0 + 0]
                id: Integer(:32 + 0)
                ofs: Integer(:32 + 0)
              end
              Priority: array [:0 + 4] of bit
            end
        end
        ModParams: array [:7 + 0] of record[:0 + 0]
            ModId: record[:0 + 0]
              id: Integer(:32 + 0)
              ofs: Integer(:32 + 0)
            end
            n16: Integer(:16 + 0)
            n16: Integer(:16 + 0)
            n24: Integer(:24 + 0)
            n7: Integer(:7 + 0)
            n15: Integer(:15 + 0)
            f2: array [:0 + 2] of bit
            fil: array [:0 + 74] of bit
            s2mv: array [:6 + 0] of record[:0 + 0]
                m_FileType: array [:0 + 4] of Byte
                m_Realm: array [:0 + 4] of Byte
                m_SHA256Hash: array [:0 + 32] of Byte
              end
            flag: array [:0 + 1] of bit
            m_stringToon: record[:0 + 0]
              m_region: Integer(:8 + 0)
              m_programId: array [:0 + 32] of bit
              m_realm: Integer(:32 + 0)
              m_globalName: array [:7 + 2] of Byte
            end
            m_toon: record[:0 + 0]
              m_region: Integer(:8 + 0)
              m_programId: array [:0 + 32] of bit
              m_realm: Integer(:32 + 0)
              m_id: Integer(:64 + 0)
            end
            trttt: record[:0 + 0]
              b32: Optional:1 of (array [:0 + 32] of bit)
              b23: Optional:1 of (array [:0 + 23] of bit)
              b1: array [:0 + 1] of bit
              b32: Optional:1 of (array [:0 + 32] of bit)
              b3: array [:0 + 3] of bit
              b30: Integer(:30 + 0)
              b3: array [:0 + 3] of bit
            end
            filler: record[:0 + 0]
              word: array [:0 + 16] of bit
              b8: array [:0 + 8] of bit
              b8: array [:0 + 8] of bit
              b34: array [:0 + 34] of bit
              f54: Optional:1 of (array [:0 + 54] of bit)
              b1: array [:0 + 1] of bit
              b5: array [:0 + 5] of bit
              b5: array [:0 + 5] of bit
              b5: array [:0 + 5] of bit
            end
            bbbb: record[:0 + 0]
              ModId: record[:0 + 0]
                id: Integer(:32 + 0)
                ofs: Integer(:32 + 0)
              end
              n32: Integer(:32 + 0)
              f: array [:0 + 1] of bit
              n21: Integer(:21 + 0)
              CAFEBABE: Integer(:32 + 0)
            end
            fil28: Integer(:28 + 0)
            fil: array [:0 + 36] of bit
            hero: Optional:1 of (record[:0 + 0]
                b11: array [:0 + 11] of bit
                a93: array [:4 + 0] of record[:0 + 0]
                    num: Integer(:6 + 0)
                    b32: Integer(:32 + 0)
                    b16: Integer(:16 + 0)
                    b16: Integer(:16 + 0)
                    b23: Integer(:23 + 0)
                  end
                b4: array [:0 + 4] of bit
                a8*5: case (:4 + 0) of
                  None(0): array [:0 + 0] of bit
                  None(1): array [:0 + 0] of bit
                  None(2): array [:0 + 0] of bit
                  None(3): array [:0 + 0] of bit
                  None(4): array [:0 + 0] of bit
                  Data(5): record[:0 + 0]
                    b40: array [:0 + 40] of bit
                    b16: array [:0 + 16] of bit
                    b79: array [:0 + 79] of bit
                    b160: array [:0 + 160] of bit
                    b105: array [:0 + 105] of bit
                  end
                end
                a23: array [:7 + 0] of array [:0 + 23] of bit
                b11: array [:0 + 11] of bit
                bb: Optional:1 of (record[:0 + 0]
                    b38: array [:0 + 38] of bit
                    b16: Integer(:16 + 0)
                    b16: Integer(:16 + 0)
                  end)
                b1: array [:0 + 1] of bit
                hero: array [:5 + 0] of array [:0 + 32] of bit
                b23: array [:0 + 23] of bit
              end)
            ModDependencies: array [:6 + 0] of record[:0 + 0]
                id: Integer(:32 + 0)
                ofs: Integer(:32 + 0)
              end
            fil: array [:0 + 32] of bit
          end
        s2mh: array [:6 + 0] of record[:0 + 0]
            m_FileType: array [:0 + 4] of Byte
            m_Realm: array [:0 + 4] of Byte
            m_SHA256Hash: array [:0 + 32] of Byte
          end
        skins: array [:16 + 0] of array [:0 + 64] of bit
        hasSkins: array [:32 + 0] of array [:0 + 256] of bit
        InitData: record[:0 + 0]
          m_disabledHeroList: array [:8 + 0] of array [:0 + 32] of bit
          m_randomSeed: array [:0 + 32] of bit
          unk: array [:0 + 32] of bit
        end
        playersInfo: array [:5 + 0] of record[:0 + 0]
            m_Unk1: record[:0 + 0]
              m_Unk1: array [:0 + 32] of bit
              m_SlotId: array [:0 + 5] of bit
              m_toon: record[:0 + 0]
                m_region: Integer(:8 + 0)
                m_programId: array [:0 + 32] of bit
                m_realm: Integer(:32 + 0)
                m_id: Integer(:64 + 0)
              end
              m_Name: record[:0 + 0]
                m_stringToon: record[:0 + 0]
                  m_region: Integer(:8 + 0)
                  m_programId: array [:0 + 32] of bit
                  m_realm: Integer(:32 + 0)
                  m_globalName: array [:7 + 2] of Byte
                end
                m_Flags: array [:0 + 1] of bit
              end
              m_Unk4: array [:0 + 2] of bit
              m_SecName: Optional:1 of (record[:0 + 0]
                  m_Unk1: array [:0 + 2] of bit
                  m_stringToon: record[:0 + 0]
                    m_region: Integer(:8 + 0)
                    m_programId: array [:0 + 32] of bit
                    m_realm: Integer(:32 + 0)
                    m_globalName: array [:7 + 2] of Byte
                  end
                  m_Flags: array [:0 + 1] of bit
                end)
            end
            m_Unk2: array [:0 + 198] of bit
            m_Unk3: Optional:1 of (array [:0 + 64] of bit)
            m_Unk4: record[:0 + 0]
              m_UnkFlags1: array [:0 + 2] of bit
              m_Unk1: array [:0 + 35] of bit
              m_hasSilencePenalty: array [:0 + 1] of bit
              m_Unk2: array [:0 + 1] of bit
              m_hasVoiceSilencePenalty: array [:0 + 1] of bit
              m_isBlizzardStaff: array [:0 + 1] of bit
            end
            m_PartyInfo: Optional:1 of (array [:0 + 64] of bit)
            m_TagInfo: Optional:1 of (array [:7 + 0] of Byte)
            m_PlayerLevel: array [:0 + 32] of bit
            m_hasActiveBoost: array [:0 + 1] of bit
          end
        _end: record[:0 + 0]
          sss: array [:0 + 64] of bit
          m_toon: case (:1 + 0) of
            filler(0): array [:0 + 16] of bit
            m_toon(1): record[:0 + 0]
              m_region: Integer(:8 + 0)
              m_programId: array [:0 + 32] of bit
              m_realm: Integer(:32 + 0)
              m_id: Integer(:64 + 0)
            end
          end
          b87: array [:0 + 87] of bit
          a38: array [:4 + 1] of array [:0 + 38] of bit
          Unk: array [:0 + 1] of bit
          Neut: array [:4 + 1] of array [:0 + 32] of bit
          Hero: array [:5 + 0] of record[:0 + 0]
              b32: Integer(:32 + 0)
              HeroIcon: array [:11 + 0] of record[:0 + 0]
                  Hero: array [:0 + 32] of bit
                  ICON: Integer(:32 + 0)
                  b32: Integer(:32 + 0)
                end
              b11: array [:0 + 11] of bit
            end
          CSTM: array [:6 + 0] of array [:0 + 32] of bit
          a48: array [:5 + 0] of record[:0 + 0]
              b32: Integer(:32 + 0)
              b16: array [:0 + 16] of bit
            end
          b23: array [:0 + 23] of bit
          b32: array [:0 + 32] of bit
          _end_filler: array [:0 + 10] of bit
          b32: array [:0 + 32] of bit
          AllHeroes: array [:10 + 0] of record[:0 + 0]
              Name: array [:0 + 32] of bit
              b5: array [:0 + 5] of bit
              b128: array [:0 + 128] of bit
            end
          NewField: array [:0 + 2] of bit
        end
      end