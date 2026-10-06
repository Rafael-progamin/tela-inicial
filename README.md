# tela-inicial
import { StyleSheet, Text, View, Image, Pressable, ScrollView } from 'react-native';
import { StatusBar } from "expo-status-bar";

export default function App() {
  return (
    <View style={style_geral.container}>

      {/* CABEÇALHO */}
      <View style={style_section.head}>
        <View>
          <Text style={style_texto.title}>MARTE // COLÔNIA</Text>
          <Text style={style_texto.subtitle}>SETOR A-07 • BASE HORIZONTE</Text>
        </View>

        <Image
          style={style_geral.logo}
          source={{
            uri: 'https://images.unsplash.com/photo-1614728894747-a83421e2b9c9?auto=format&fit=crop&q=80&w=200'
          }}
        />
      </View>

      {/* CONTEÚDO */}
      <View style={style_section.body}>
        <ScrollView style={{ padding: 15 }}>

          {/* PERFIL */}
          <View style={style_geral.perfilContainer}>
            <Image
              style={style_geral.avatar}
              source={{
                uri: 'https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?auto=format&fit=crop&q=80&w=200'
              }}
            />

            <View>
              <Text style={style_texto.perfilNome}>
                Explorador Marciano
              </Text>

              <Text style={style_texto.perfilRank}>
                Colono: Novato | Nível: 1
              </Text>
            </View>
          </View>

          {/* CARTÃO 1 */}
          <Pressable style={style_components.card}>
            <Image
              style={style_components.cardImage}
              source={{
                uri: 'https://images.unsplash.com/photo-1614728894747-a83421e2b9c9?auto=format&fit=crop&q=80&w=300'
              }}
            />

            <View style={style_components.cardTextContainer}>
              <Text style={style_texto.cardTitle}>
                Exploração de Marte
              </Text>

              <Text style={style_texto.cardDesc}>
                Explore o terreno marciano e descubra novas regiões para expansão da colônia.
              </Text>
            </View>
          </Pressable>

          {/* CARTÃO 2 */}
          <Pressable style={style_components.card}>
            <Image
              style={style_components.cardImage}
              source={{
                uri: 'https://images.unsplash.com/photo-1446776811953-b23d57bd21aa?auto=format&fit=crop&q=80&w=300'
              }}
            />

            <View style={style_components.cardTextContainer}>
              <Text style={style_texto.cardTitle}>
                Sobrevivência
              </Text>

              <Text style={style_texto.cardDesc}>
                Aprenda a administrar oxigênio, água e energia longe da Terra.
              </Text>
            </View>
          </Pressable>

          {/* CARTÃO 3 */}
          <Pressable style={style_components.card}>
            <Image
              style={style_components.cardImage}
              source={{
                uri: 'https://images.unsplash.com/photo-1451187580459-43490279c0fa?auto=format&fit=crop&q=80&w=300'
              }}
            />

            <View style={style_components.cardTextContainer}>
              <Text style={style_texto.cardTitle}>
                Engenharia da Colônia
              </Text>

              <Text style={style_texto.cardDesc}>
                Construa módulos habitacionais, sistemas de energia e novas estruturas.
              </Text>
            </View>
          </Pressable>

          {/* CARTÃO 4 */}
          <Pressable style={style_components.card}>
            <Image
              style={style_components.cardImage}
              source={{
                uri: 'https://images.unsplash.com/photo-1517976547714-720226b864c1?auto=format&fit=crop&q=80&w=300'
              }}
            />

            <View style={style_components.cardTextContainer}>
              <Text style={style_texto.cardTitle}>
                Comunicação Orbital
              </Text>

              <Text style={style_texto.cardDesc}>
                Mantenha contato com a Terra e monitore os satélites da colônia.
              </Text>
            </View>
          </Pressable>

        </ScrollView>
      </View>

      {/* RODAPÉ */}
      <View style={style_section.footer}>

        <Pressable style={style_components.tab}>
          <Text style={style_texto.tabTextActive}>
            COLÔNIA
          </Text>
        </Pressable>

        <Pressable style={style_components.tab}>
          <Text style={style_texto.tabText}>
            MISSÕES
          </Text>
        </Pressable>

        <Pressable style={style_components.tab}>
          <Text style={style_texto.tabText}>
            MAPA
          </Text>
        </Pressable>

        <Pressable style={style_components.tab}>
          <Text style={style_texto.tabText}>
            PERFIL
          </Text>
        </Pressable>

      </View>

      <StatusBar style="light" />
    </View>
  );
}


/* =========================
   ESTILOS GERAIS
========================= */

const style_geral = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#120d0b',
    maxWidth: 400,
  },

  logo: {
    width: 48,
    height: 48,
    borderRadius: 24,
    marginRight: 10,
    borderWidth: 2,
    borderColor: '#e05232',
  },

  perfilContainer: {
    flexDirection: 'row',
    alignItems: 'center',
    backgroundColor: '#211512',
    padding: 15,
    borderRadius: 8,
    marginBottom: 20,

    borderLeftWidth: 4,
    borderColor: '#e05232',
  },

  avatar: {
    width: 50,
    height: 50,
    borderRadius: 25,
    marginRight: 15,

    backgroundColor: '#333',

    borderWidth: 2,
    borderColor: '#e05232',
  }
});


/* =========================
   TEXTOS
========================= */

const style_texto = StyleSheet.create({

  title: {
    fontSize: 21,
    fontWeight: 'bold',
    color: '#e05232',
    marginLeft: 15,
    letterSpacing: 2,
  },

  subtitle: {
    fontSize: 10,
    color: '#8f766d',
    marginLeft: 15,
    marginTop: 3,
    letterSpacing: 1,
  },

  perfilNome: {
    color: '#ffffff',
    fontSize: 16,
    fontWeight: 'bold',
  },

  perfilRank: {
    color: '#a98f84',
    fontSize: 13,
    marginTop: 3,
  },

  cardTitle: {
    color: '#ffffff',
    fontSize: 16,
    fontWeight: 'bold',
    marginBottom: 5,
  },

  cardDesc: {
    color: '#a98f84',
    fontSize: 13,
    lineHeight: 18,
  },

  tabText: {
    color: '#8f766d',
    fontSize: 11,
    fontWeight: '600',
  },

  tabTextActive: {
    color: '#e05232',
    fontSize: 11,
    fontWeight: 'bold',
  }
});


/* =========================
   SEÇÕES
========================= */

const style_section = StyleSheet.create({

  head: {
    borderBottomWidth: 1,
    borderColor: '#4a3028',

    justifyContent: 'space-between',
    alignItems: 'center',

    flexDirection: 'row',

    flex: 1.5,

    backgroundColor: '#17100e',
  },

  body: {
    flex: 9,
  },

  footer: {
    borderTopWidth: 2,
    borderColor: '#4a3028',

    flex: 1.5,

    flexDirection: 'row',
    justifyContent: 'space-around',
    alignItems: 'center',

    padding: 10,

    backgroundColor: '#17100e',
  },
});


/* =========================
   COMPONENTES
========================= */

const style_components = StyleSheet.create({

  card: {
    backgroundColor: '#211512',

    flexDirection: 'row',

    borderRadius: 8,

    marginBottom: 15,

    borderWidth: 1,
    borderColor: '#36221d',

    overflow: 'hidden',
  },

  cardImage: {
    width: 100,
    height: 100,
  },

  cardTextContainer: {
    flex: 1,

    padding: 15,

    justifyContent: 'center',
  },

  tab: {
    padding: 10,

    alignItems: 'center',
    justifyContent: 'center',
  }
});
